**`/*自动登录网页，自动填写用户名，密码*/`**
1.code：

#coding = utf-8
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import os,time

driver = webdriver.Firefox()
driver.get("http://192.168.19.45:4020")
time.sleep(3)
driver.maximize_window()
driver.find_element_by_id("UserName").clear()
driver.find_element_by_id("UserName").send_keys("admin")
driver.find_element_by_id("UserName").send_keys(Keys.TAB)
time.sleep(3)
driver.find_element_by_id("Password").send_keys("123456")
driver.find_element_by_id("Password").send_keys(Keys.ENTER)
time.sleep(5)
driver.quit()



ps：主要是没有验证码的，登录