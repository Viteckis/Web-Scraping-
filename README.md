# Web-Scraping-
Web Scraping with Selenium
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

driver = webdriver.Chrome()
driver.get("https://example.com")

search_box = driver.find_element("name", "q")
search_box.send_keys("Python")
search_box.send_keys(Keys.RETURN)

results = driver.find_elements_by_css_selector(".search-results-item")
for result in results:
    print(result.text)

driver.quit()
