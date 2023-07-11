```yml
1.LocalDate转Date
 
LocalDate nowLocalDate = LocalDate.now();
Date date = Date.from(localDate.atStartOfDay(ZoneOffset.ofHours(8)).toInstant());
 
2.LocalDateTime转Date
 
LocalDateTime localDateTime = LocalDateTime.now();
Date date = Date.from(localDateTime.atZone(ZoneOffset.ofHours(8)).toInstant());
 
3.Date转LocalDateTime(LocalDate)
 
Date date =newDate();
LocalDateTime localDateTime = date.toInstant().atZone(ZoneOffset.ofHours(8)).toLocalDateTime();
LocalDate localDate = date.toInstant().atZone(ZoneOffset.ofHours(8)).toLocalDate();
 
4.LocalDate转时间戳
 
LocalDate localDate = LocalDate.now();
longtimestamp = localDate.atStartOfDay(ZoneOffset.ofHours(8)).toInstant().toEpochMilli();
 
5.LocalDateTime转时间戳
 
LocalDateTime localDateTime = LocalDateTime.now();
longtimestamp = localDateTime.toInstant(ZoneOffset.ofHours(8)).toEpochMilli();
 
6.时间戳转LocalDateTime(LocalDate)
 
longtimestamp = System.currentTimeMillis();
LocalDate localDate = Instant.ofEpochMilli(timestamp).atZone(ZoneOffset.ofHours(8)).toLocalDate();
LocalDateTime localDateTime = Instant.ofEpochMilli(timestamp).atZone(ZoneOffset.ofHours(8)).toLocalDateTime();
```

