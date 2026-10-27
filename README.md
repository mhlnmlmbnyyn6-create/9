from selenium import webdriver
from selenium.webdriver.common.by import By
import time

# تشغيل المتصفح
driver = webdriver.Chrome()
driver.get("https://pocketoption.com/")

# انتظر حتى تقوم بتسجيل الدخول يدوياً أو برمجياً
time. الخيار = input("اضغط Enter بعد تسجيل الدخول يدويًا وتجهيز المنصة...")

# مثال لضغط زر صعود (Call) - يعتمد على الـ XPath الخاص بالزر في المنصة
try:
    call_button = driver.find_element(By.XPATH, "//button[contains(@class, 'success')]")
    call_button.click()
    print("تم تنفيذ صفقة صعود بنجاح!")
except Exception as e:
    print("حدث خطأ أثناء تنفيذ الصفقة:", e)

time.sleep(5)
driver.quit()
# 9
