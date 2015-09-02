# babel-sublime

ชุดภาษาสำหรับ [ES6+ JavaScript](http://kangax.github.io/compat-table/es6/) มาพร้อมกับส่วนเสริม [React JSX syntax](http://facebook.github.io/react/docs/jsx-in-depth.html) extensions.

## การติดตั้ง

ค้นหาชื่อ [**Babel**](https://packagecontrol.io/packages/Babel) ผ่าน [Package Control](https://packagecontrol.io/) ใน Sublime Text (ที่ติดตั้งระบบ Package Control แล้ว)

#### วิธีตั้งค่าให้เป็น syntax เริ่มต้น

วิธีตั้งค่าให้เป็น syntax เริ่มต้นกับไฟล์ที่มีนามสกุลเฉพาะที่ต้องการ:
  1. เปิดไฟล์นามสกุลที่ต้องการขึ้นมา (ไฟล์อะไรก็ได้ เช่น .js),
  2. เปิดเมนู `View` จากแถบเมนูด้านบน,
  3. เลือก `Syntax` `->` `Open all with current extension as...` `->` `Babel` `->` `JavaScript (Babel)`.
  4. ทำแบบเดียวกันกับไฟล์ฟอร์แมตอื่นๆ  (เช่น: `.jsx`).

#### วิธีตั้งค่าธีมสี

`Babel` มีชุดธีมสีเริ่มต้นชื่อ `Next` และ `Monokai` จาก [Benvie/JavaScriptNext.tmLanguage](https://github.com/Benvie/JavaScriptNext.tmLanguage). สามารถเลือกสีได้โดยไปที่เมนู `Preferences` `->` `Color Scheme` `->` `Babel`

#### การใช้งานขั้นสูง

ถ้าต้องการ พวกเราสามารถตั้งค่าให้  `Babel` as the _only_ JavaScript package โดยไปปิดการทำงานของ Javascript package มาตรฐาน
ทำได้โดย ไปเพิ่ม `"ignored_packages": ["JavaScript"]` ใน `Preferences.sublime-settings`. 
ซึ่งทำให้ได้ความสะดวกมา 2 อย่างนั่นคือ:
  * Node script ที่ไม่ระบุนามสกุลไฟล์ทั้งหลาย จะถูกมองเป็น `JavaScript (Babel)` โดยอัตโนมัติ,
  * ทำให้ Syntax menu สะอาดตาขึ้น.

**ระวังไว้ด้วย**, การเปลี่ยนแปลงนี้อาจจะทำให้ snippet มาตรฐานไม่ทำงาน (ถือว่าเลือกเองนะ), และ package อื่นๆ ที่อ้างอิงกับ Javascript package มาตรฐานมีโอกาสเจ๊งสูง ตรงนี้ทีมงานไม่รับประกัน

## ภาพตัวอย่างการใช้งาน

![babel-sublime-vs-sublime-react--react-class](https://raw.githubusercontent.com/babel/babel-sublime/45c7d37/screenshots/compare-react-class@2x.png)

* `babel-sublime` รองรับ JavaScript syntax ยุคใหม่, รวมถึง [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions), [destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment), [shorthand methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions), [template strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/template_strings), และอื่นๆ อีกมากมาย.

![babel-sublime-vs-sublime-react--jsx-comments-etc](https://raw.githubusercontent.com/babel/babel-sublime/9a6e85f/screenshots/compare-jsx-comments-etc@2x.png)

* `babel-sublime` สามารถแยกแยะ JSX comments ระหว่าง attributes, namespaced components, และ non-alpha characters ในชื่อ tag หรือ attribute ได้อย่างถูกต้อง.

![babel-sublime-vs-sublime-react--jsx-illegal](https://raw.githubusercontent.com/babel/babel-sublime/9a6e85f/screenshots/compare-jsx-illegal@2x.png)

* ไฮไลท์การเขียนที่ผิดใน JSX attribute names; ลืมเครื่องหมาย equals, quotes หรือ braces; และลืมใส่ค่า values, ทำให้ตรวจสอบส่วนที่ผิดพลาดได้ง่ายขึ้น.

![babel-sublime-vs-sublime-react--jsx-tight](https://raw.githubusercontent.com/babel/babel-sublime/9a6e85f/screenshots/compare-jsx-tight@2x.png)

* เครื่องหมายมากกว่า/น้อยกว่า จะแยกอย่างชัดเจนจากการเขียน JSX .

## Snippets

ติดตั้ง Snippets ที่แยกไว้อีก Package ต่างหากได้จาก [babel/babel-sublime-snippets](https://github.com/babel/babel-sublime-snippets) หรือ [**Babel Snippets**](https://packagecontrol.io/packages/Babel Snippets) ผ่านระบบ [Package Control](https://packagecontrol.io/).

## อื่นๆ

#### [Oceanic Next Color Scheme](https://github.com/voronianski/oceanic-next-theme)

[![](https://raw.githubusercontent.com/voronianski/babel-sublime/master/screenshots/oceanic-next.png)](https://github.com/voronianski/oceanic-next-theme)

ชุดธีมสีของ Sublime Text ที่รองรับการเขียนแบบใหม่ๆ ใน JavaScript และ babel-sublime package.

#### [Zeus Color Scheme](https://github.com/zaynali53/Zeus-Theme)

![zeus-color-scheme](https://raw.githubusercontent.com/zaynali53/Zeus-Theme/master/Zeus-Color-Scheme.PNG)

## About

ภาษาไทย และแนะนำให้ใช้โดย โค้ชพล ธีรเศรษฐ์ จิรภัทร์ชาญเดช

Under the hood, _babel-sublime_ is based on the excellent [Benvie/JavaScriptNext.tmLanguage](https://github.com/Benvie/JavaScriptNext.tmLanguage) with JSX syntax support built on top. The initial definitions for JSX came from [reactjs/sublime-react](https://github.com/reactjs/sublime-react) via [yungters/sublime](https://github.com/yungsters/sublime.git) - special thanks go to [@jgebhardt](https://github.com/jgebhardt) and [@zpao](https://github.com/zpao).

## Contributing

Pull Requests should include your changes to the respective `YAML-tmKittens` file as well as the converted `tmKittens` file. Use [AAAPackageDev](https://github.com/SublimeText/AAAPackageDev) to convert the `YAML-tmKittens` files.
