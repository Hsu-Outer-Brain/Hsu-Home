# 常用命令

{% tabs %}
{% tab title="date" %}
```python
import time，datetime

# 时间戳转时间字符串（timestamp to datetimeStr）
def timestampToDateStr(stamps, frmt='%Y-%m-%d %H:%M:%S'):
#     return time.strftime(frmt, time.localtime(stamps))
    return datetime.fromtimestamp(stamps).strftime(frmt)

# 时间字符串转时间戳（datetimeStr to timestamp）
def dateStrToTimestamp(str_, frmt='%Y-%m-%d %H:%M:%S'):
#     return time.mktime(datetime.strptime(str_, frmt).timetuple())
    return time.mktime(time.strptime(str_, frmt))

# 时间字符串转时间（datetimeStr to datetime）
def dateStrToDate(str_, frmt='%Y-%m-%d %H:%M:%S'):
    return datetime.strptime(str_, frmt)

# 时间转时间字符串（datetime to datetimeStr）
def dateToDateStr(date_, frmt='%Y-%m-%d %H:%M:%S'):
    return date_.strftime(frmt)

# 时间戳转时间（datetime to timestamp）
def timestampToDate(stamps):
    return datetime.fromtimestamp(stamps)

# 时间转时间戳（timestamp to datetime）
def dateToTimestamp(date_):
    return time.mktime(date_.timetuple())

# 获取指定格式的当前时间
time.strftime("%Y%m%d%H%M%S", time.gmtime())
# '20190226090628'

# 测试用例
dateStr = '2018-06-02 12:12:12'
stamps = 1527912732.0
lenth = 10
print(timestampToDateStr(stamps), type(timestampToDateStr(stamps)))
print(dateStrToTimestamp(dateStr), type(dateStrToTimestamp(dateStr)))
print(dateStrToDate(dateStr), type(dateStrToDate(dateStr)))
print(dateToDateStr(dateStrToDate(dateStr)), type(dateToDateStr(dateStrToDate(dateStr))))
print(timestampToDate(stamps), type(timestampToDate(stamps)))
print(dateToTimestamp(dateStrToDate(dateStr)), type(dateToTimestamp(dateStrToDate(dateStr))))
```
{% endtab %}
{% endtabs %}



