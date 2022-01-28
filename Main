from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.chrome.options import Options

#Name of Image to be scraped
val = input("Enter your image name: ")

#Makes chrome headless
chrome_options = Options()
chrome_options.add_argument("--headless")
web = webdriver.Chrome(options=chrome_options)

#Go to google Images and input The name of the image
web.get('https://images.google.com/')
InputXpath = web.find_element_by_xpath("/html/body/div[1]/div[3]/form/div[1]/div[1]/div[1]/div/div[2]/input")
InputXpath.send_keys(val)
InputXpath.send_keys(Keys.ENTER)

#Find the Image
image = web.find_element_by_xpath("//img[contains(@class,'Q4LuWd')]")

#Takes in File Location
val2 = input("Enter your File Location: ")
#Writes to File
image.screenshot(val2)

#Close Web
web.close();


