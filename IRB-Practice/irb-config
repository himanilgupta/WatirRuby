require 'watir'
browser=Watir::Browser.new:chrome
browser.goto “http://watir.com/examples/forms_with_input_elements.html”
 

t1=browser.text_field id: 'new_user_first_name'
t1.set "Testing"
t2=browser.text_field id: 'new_user_last_name'
t2.set “testdata"
 

sl=browser.select_list id: 'new_user_languages'
sl.select 'English'
sl.selected_options
 

rd=browser.radio value: 'no'
rd.set
chk=browser.checkbox value: 'cars'
chk.set
 
#Here we will see how to click button.
btn=browser.button name: 'new_user_button_2'
btn.click
 

Watir::Wait.until {browser.text.include? 'submit'}
 

if browser.text.include? "submit"
puts "Data Submitted"
else
puts "Data not yet submitted"
end
 

browser.driver.manage.timeouts.implicit_wait = 30
 

browser.send_keys :page_up
 

browser.screenshot.save ‘screenshot1.png'
 
browser.send_keys :page_down
browser.screenshot.save ‘screenshot2.png'
 
puts "TestCase Executed"
browser.close
