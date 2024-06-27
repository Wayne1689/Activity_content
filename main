import selenium
import time
import random #以實現隨機IP
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.options import Options

#前往網站跟瀏覽器設定
opt = Options()
opt.add_argument('--ignore-certificate-errors')
driver = webdriver.Chrome(options=opt)
driver.get('https://sys.ndhu.edu.tw/SA/XSL_ApplyRWD/ActApply.aspx')
driver.find_element(By.ID,'BodyContent_gvActs_lbtGridShow_0').click()

#抓取文檔
text_element = driver.find_element(By.ID,'BodyContent_txt_act_content')
text_content = text_element.text

#用來將文檔寫入指定路徑
file_path = r"C:/Users/s3919/OneDrive/桌面/爬取的文檔/Web_content.txt"

with open(file_path, "w", encoding="utf-8") as file:
    file.write(text_content)
