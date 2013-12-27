#Calendar

日历组件

##ATTR属性

* date {Date, String} [可选] [默认值：null] 初始化日期，默认今天

* firstDay {Number} [可选] [默认值：1] 设置新的一周从星期几开始，星期天用0表示, 星期一用1表示, 以此类推.

* maxDate {Date, String} [可选] [默认值：null] 设置可以选择的最大日期

* minDate {Date, String} [可选] [默认值：null] 设置可以选择的最小日期

* swipeable {Boolean} [可选] [默认值：false] 设置是否可以通过左右滑动手势来切换日历

* monthChangeable {Boolean} [可选] [默认值：false] 设置是否让月份可选择

* yearChangeable {Boolean} [可选] [默认值：false] 设置是否让年份可选择

##事件

| 事件名 | 描述 | 参数说明 |
| ---- | ---- | ---- | 
| ready | 当组件初始化完后触发。 | e {Event}Event对象 |
| select | 选中日期的时候触发 | e {Event}Event对象 <br> date {Date}当前选中的日期 <br> dateStr {String}当前选中日期的格式化字符串 <br> instance {Instance}当前日历的实例 |
| monthchange | 当前显示月份发生变化时触发 | e {Event}Event对象 <br> month {Date}当前月份 <br> year {String}当前年份 <br> instance {Instance}当前日历的实例 |
| destroy | 组件在销毁的时候触发 | e {Event}Event对象 |

##方法

* **switchToToday**

	切换到今天所在月份

* **switchMonthTo**

	切换月份

		参数:
		
		month {String, Number}目标月份，值可以为+1M, +4M, -5Y, +1Y等等。+1M表示在显示的月的基础上显示下一个月，+4m表示下4个月，-5Y表示5年前
		year {String, Number}目标年份

		返回值:
	
		{self}返回本身
	

* **refresh**

	刷新日历，当修改attr后需要调用此方法

		返回值:

		{self}返回本身
	

* **destroy**

	销毁组件

* **maxDate**

	设置或获取maxDate，如果想要设置生效需要调用Refresh方法

		参数:
	
		value {String, Date}最大日期的值
	
		返回值:
	
		{self}返回本身


* **minDate**

	设置或获取minDate，如果想要设置生效需要调用Refresh方法

		参数:

		value {String, Date}最小日期的值
		
		返回值:
		
		{self}返回本身


* **date**

	设置或获取当前日期，如果想要设置生效需要调用Refresh方法

		参数:
		
		value {String, Date}当前日期
		
		返回值:
		
		{self}返回本身


* **selectedDate**

	设置或获取当前选中的日期，如果想要设置生效需要调用Refresh方法

		参数:
		
		value {String, Date}要选中的日期
		
		返回值:
		
		{self}返回本身

