# Selenium
1. python Selenium 判断 Classname 有多个的时候，在检查的页面点击Console 输入 document.getElementByClassName("##")
2. Win 10 系统下， 利用wendriver 打开IE浏览器，driver=webdriver.Edge()
3. 判断打开页面是否正确时，可以检查页面元素，但是不能检查url,因为页面还没加载出来。也可以通过检查左上角的title, 具体实现方法：
    from selenium import webdriver
    from selenium. webdriver.support import expected_conditions as EC
    driver=webdriver.Chorme()
    driver.get("http://www.5itest.cn/register")
    EC.tile_contains("注册")
4. 使用xpath进行定位时，双引号内还有双引号，需要把内部的双引号变为单引号,例：
    driver.find_element_by_xpath("//*[@id='captcha_code']").send_keys("123456")
    从网页直接copy的xpath是//*[@id="captcha_code"]
5.使用class_name 定位时有多个相同的时候，使用其父系class name区分，例：
    driver.find_element_by_class_name("").find_element_by_class_name("")
 
