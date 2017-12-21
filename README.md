
原地址在 [vue-router](https://github.com/vuejs/vue-router)

### 说明

很多时候我们需要知道一次router跳转是我们自己的行为（push, replace）还是浏览器的行为（前进，后退，地址栏手动输入），类似react的history就为我们提供了一个action来标识这些（PUSH，REPLACE，POP）

所以这里对vue-router做了一些简单的修改，使我们在导航守卫里可以接收到这样一个参数

### 例子

	router.beforeEach((to, from, next, action) => {
	  console.log(action)
	  next()
	})
	router.afterEach((to, from, action) => {
	  console.log(action)
	})
