# bahttext

[![Codecov](https://img.shields.io/codecov/c/github/jojoee/bahttext.svg)](https://codecov.io/github/jojoee/bahttext)
[![Version - npm](https://img.shields.io/npm/v/bahttext.svg)](https://www.npmjs.com/package/bahttext)
[![License - npm](https://img.shields.io/npm/l/bahttext.svg)](http://opensource.org/licenses/MIT)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?style=flat-square)](https://github.com/semantic-release/semantic-release) [![Greenkeeper badge](https://badges.greenkeeper.io/jojoee/bahttext.svg)](https://greenkeeper.io/)
![continuous integration](https://github.com/jojoee/bahttext/workflows/continuous%20integration/badge.svg?branch=master)
![release](https://github.com/jojoee/bahttext/workflows/release/badge.svg?branch=master)
![runnable](https://github.com/jojoee/bahttext/workflows/runnable/badge.svg?branch=master)
![runnable old node](https://github.com/jojoee/bahttext/workflows/runnable%20old%20node/badge.svg?branch=master)

ภาษา: [ไทย](https://github.com/jojoee/bahttext/blob/master/README.md), [English](https://github.com/jojoee/bahttext/blob/master/README-en.md)

เปลี่ยนตัวเลข เป็นคำอ่านภาษาไทย, โมดูลตัวนี้ได้ทำการทดสอบกับ [Google Sheets BAHTTEXT function](https://support.google.com/docs/answer/9982303?hl=en), [Demo page](https://jojoee.github.io/bahttext/) เรียบร้อยแล้ว

## ติดตั้ง

```
// ติดตั้งด้วย CommonJS
npm install bahttext
const { bahttext } = require('bahttext')

// ติดตั้งด้วย Bower
bower install bahttext
<script src="bower_components/bahttext/src/index.js"></script>

// ติดตั้งด้วย githack
<script src="https://raw.githack.com/jojoee/bahttext/master/src/index.js"></script>

// ติดตั้งด้วย ES6
npm install bahttext
import { bahttext } from "bahttext"
```

## ตัวอย่างการใช้งาน

```javascript
bahttext(8.00) // แปดบาทถ้วน
bahttext(5678.00) // ห้าพันหกร้อยเจ็ดสิบแปดบาทถ้วน
bahttext(63147.89) // หกหมื่นสามพันหนึ่งร้อยสี่สิบเจ็ดบาทแปดสิบเก้าสตางค์
bahttext(51000001.00) // ห้าสิบเอ็ดล้านหนึ่งบาทถ้วน
bahttext(317.10) // สามร้อยสิบเจ็ดบาทสิบสตางค์
bahttext(422.26) // สี่ร้อยยี่สิบสองบาทยี่สิบหกสตางค์
bahttext(11.11) // สิบเอ็ดบาทสิบเอ็ดสตางค์
bahttext(191415.11) // หนึ่งแสนเก้าหมื่นหนึ่งพันสี่ร้อยสิบห้าบาทสิบเอ็ดสตางค์
bahttext(1.01) // หนึ่งบาทหนึ่งสตางค์
bahttext(5678.46) // ห้าพันหกร้อยเจ็ดสิบแปดบาทสี่สิบหกสตางค์
bahttext(0.67) // หกสิบเจ็ดสตางค์
bahttext(-3.00) // ลบสามบาทถ้วน
bahttext(-232.00) // ลบสองร้อยสามสิบสองบาทถ้วน
bahttext(-44444.00) // ลบสี่หมื่นสี่พันสี่ร้อยสี่สิบสี่บาทถ้วน
bahttext(-5678934.00) // ลบห้าล้านหกแสนเจ็ดหมื่นแปดพันเก้าร้อยสามสิบสี่บาทถ้วน
bahttext(-201.00) // ลบสองร้อยหนึ่งบาทถ้วน
bahttext(-317.10) // ลบสามร้อยสิบเจ็ดบาทสิบสตางค์
bahttext(-5723.00) // ลบห้าพันเจ็ดร้อยยี่สิบสามบาทถ้วน
bahttext(-11.00) // ลบสิบเอ็ดบาทถ้วน
bahttext(-45621.21) // ลบสี่หมื่นห้าพันหกร้อยยี่สิบเอ็ดบาทยี่สิบเอ็ดสตางค์
bahttext(-191415.11) // ลบหนึ่งแสนเก้าหมื่นหนึ่งพันสี่ร้อยสิบห้าบาทสิบเอ็ดสตางค์
bahttext(-282622.22) // ลบสองแสนแปดหมื่นสองพันหกร้อยยี่สิบสองบาทยี่สิบสองสตางค์
bahttext(-1.04) // ลบหนึ่งบาทสี่สตางค์
bahttext(-574.45) // ลบห้าร้อยเจ็ดสิบสี่บาทสี่สิบห้าสตางค์
bahttext(-345.23) // ลบสามร้อยสี่สิบห้าบาทยี่สิบสามสตางค์
bahttext(-0.20) // ลบยี่สิบสตางค์
```

## ฟีเจอร์
- [x] สามารถใช้งานได้ทุก เบราว์เซอร์
- [x] สามารถใช้งานได้ตั้งแต่ Node.js version 6+
- [x] 0 Dependencies
- [x] ทำการทดสอบแบบ unit test
- [x] ลดการซ้ำซ้อนของการเขียน ระหว่าง code และ ไฟล์ csv ในการทำการทดสอบ
- [x] [หน้าตัวอย่างการใช้งาน](https://jojoee.github.io/bahttext/)
- [x] สนับสนุนการใช้งานกับตัวเลขติดลบ
- [x] แก้ไข semantic-release

## ภาษาอื่นๆ
- Python: [jojoee/pybaht](https://github.com/jojoee/pybaht)

## CMD

```
brew install curl
brew install jq
npm install -g csvtojson
curl -L -o ./misc/testcases.csv https://docs.google.com/spreadsheets/d/e/2PACX-1vTb8PIKzgo07rn9UpcjqE0YrdMAmf4fyDbL2plUieLCyrn_5O3vDvece7UfkaArWQLUSsaw92jVpY_z/pub?gid=0&single=true&output=csv
csvtojson ./misc/testcases.csv | jq > ./misc/testcases.json

# to update dependency version
npm update --save
npm audit fix --force
```

## อ้างอิง
- [Google Sheets BAHTTEXT function](https://support.google.com/docs/answer/9982303?hl=en)
- [Microsoft Office's BAHTTEXT function](https://support.office.com/en-us/article/BAHTTEXT-function-5ba4d0b4-abd3-4325-8d22-7a92d59aab9c)
- แรงบัลดาลใจจาก [earthchie/BAHTTEXT.js](https://github.com/earthchie/BAHTTEXT.js)
