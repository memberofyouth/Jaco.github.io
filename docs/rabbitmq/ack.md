```
	//监听
    @RabbitListener(queues = MqConstant.SUI)
    public void process(Message msg, Channel channel) {
    	//拿到消息标记
        long deliveryTag = msg.getMessageProperties().getDeliveryTag();
        try{
        	...
            //处理成功，手动ack
            channel.basicAck(deliveryTag,false);
        }catch(Excetion e){
        	try {
        		//这样容易消息堆积，可以定义死信队列接收再处理；这里拒绝就会丢到死信队列中：channel.basicReject(deliveryTag, false);
                log.info("=====处理失败，消息重新放回队列=====");
                channel.basicNack(deliveryTag,false,true);
            } catch (IOException ex) {
                ex.printStackTrace();
            }
        }
    	
    	
    	
    }
```

