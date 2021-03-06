#APP开发注意事项&原则
1. 先布局后开发
	1. 避免绝对布局, 尽可能减少适配问题
	2. 严禁为了一时的速度和任务进度, 只按照一种机型\尺寸开发
2. 一开始就约定好系统基本配色\字号, 杜绝出现任何其它颜色\字号
3. 同上, 约定好基本风格(边距\列表间距\模块间距\分割线)
	1. 此类问题如果不一开始就注意, 后期测试\修改会非常耗时间
	2. 同时为了避免初期在细节上花费过多时间, 所以只要求处理基本风格
4. 处理返回数据为空的页面展示\提示
5. 统一右拉返回风格(含导航\不含导航)
	1. 处理不好会出现导航条时隐时现
	2. 二级页面是否需要有tab导航, 最简单的逻辑是所有二级页面都不显示tab
	3. 所有二级页面都不显示tab会出现进入层级过深很难跳出的问题, 因此可以考虑部分跳转多的页面带有tab, 但要处理好在二级页面点击tab如何跳转的问题
6. 统一搜索样式\风格
	1. 首先选同一风格的搜索框\控件
	2. 其次逻辑上统一是即时搜索还是点按钮搜索
	3. 以及点取消的操作(取消搜索还是取消输入? 搜索结果是否保留?)
	4. 实际开发过程中搜索遇到的问题非常多, 一定要有一套标准的逻辑
7. 任何页面必须一开始就加标题, 即使不确定也不要留空
8. 尽可能早的用"真实数据"填充应用, 即使数据是模拟的
	1. 真实数据的展示效果跟设计稿很可能差距很大
9. 设计\约定几种图片比例
	1. 尽量标准, 比如16:9,4:3
	2. 尽量少, 不要有过多不同的比例
10. 图片严禁拉伸
	1. 所有的图片都不允许拉伸(变形), 这是一个基本原则
11. 默认图片\头像
	1. 不允许出现头像为空的情况
	2. 必须处理没有图片或图片加载不到的情况
12. 涉及删除\取消的操作需要确认
	1. 好处1减少误操作
	2. 好处2避免用户连续点击导致数据不同步问题
13. 登录状态不同, 逻辑处理
	1. 不登录哪些页面不能查看, 哪些操作不能触发, 需要有统一&严谨的逻辑
	2. 比较好的做法是涉及到登录操作的地方直接跳去登录页面, 涉及到需要根据登录状态展示不同页面的地方展示能显示的数据, 然后提示需要登录