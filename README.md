## เทมเพลตเริ่มต้นสำหรับ AWS Amplify Vue.js ภาษาไทย 🇹🇭

ที่เก็บนี้มาจากเทมเพลตเริ่มต้นของ AWS ที่ถูกปรับแต่งเพื่อรองรับการแปลเป็นภาษาไทย เทมเพลตนี้จัดเตรียมเทมเพลตเริ่มต้นสำหรับการสร้างแอปพลิเคชันโดยใช้ Vue.js และ AWS Amplify โดยเน้นความง่ายในการตั้งค่าสำหรับการตรวจสอบสิทธิ์, API, และความสามารถของฐานข้อมูล

## ภาพรวม

เทมเพลตนี้จะช่วยให้คุณมีแอปพลิเคชัน Vue พื้นฐานที่ผสานรวมกับ AWS Amplify พร้อมใช้งาน โดยออกแบบมาเพื่อรองรับการขยายตัวและประสิทธิภาพ เหมาะสำหรับนักพัฒนาที่ต้องการเริ่มต้นโครงการด้วยบริการ AWS ที่ถูกตั้งค่าไว้ล่วงหน้า เช่น Cognito, AppSync, และ DynamoDB

## คุณสมบัติ

- **การตรวจสอบสิทธิ์**: ตั้งค่าด้วย Amazon Cognito สำหรับการตรวจสอบสิทธิ์ผู้ใช้ที่ปลอดภัยพร้อมการแปลเป็นภาษาไทย 🇹🇭
- **API**: พร้อมใช้งานกับ GraphQL endpoint ด้วย AWS AppSync
- **ฐานข้อมูล**: ฐานข้อมูลเรียลไทม์ขับเคลื่อนด้วย Amazon DynamoDB

## ใบอนุญาต

ไลบรารีนี้ได้รับอนุญาตภายใต้ใบอนุญาต MIT-0 ดูไฟล์ LICENSE

## เริ่มต้นอย่างรวดเร็ว

1. โคลนหรือดาวน์โหลดที่เก็บข้อมูลนี้
2. ติดตั้งแพ็คเกจที่จำเป็นทั้งหมดของโปรเจกต์

```bash
npm install
```

3. เริ่มต้น sandbox ในเครื่อง จำเป็นต้องมีสภาพแวดล้อม AWS CLI ที่กำหนดค่าไว้แล้ว ขั้นตอนจะแนะนำวิธีตั้งค่าหากยังไม่มี

```bash
npx ampx sandbox
```

4. รันในเครื่อง

```bash
npx run dev
```

5. การเผยแพร่บน AWS สำหรับคำแนะนำโดยละเอียดในการเผยแพร่แอปพลิเคชันของคุณ โปรดดูที่[ส่วนการเผยแพร่](https://docs.amplify.aws/vue/start/quickstart/#deploy-a-fullstack-app-to-aws) ของเอกสาร AWS ตั้งแต่ขั้นตอนที่ 2


---

&nbsp;




## Thai AWS Amplify Vue.js Starter Template 🇹🇭

This repository is a from from AWS Starter Template configured for Thai localization. The template provides a starter template for creating applications using Vue.js and AWS Amplify, emphasizing easy setup for authentication, API, and database capabilities.

## Overview

This template equips you with a foundational Vue application integrated with AWS Amplify, streamlined for scalability and performance. It is ideal for developers looking to jumpstart their project with pre-configured AWS services like Cognito, AppSync, and DynamoDB.

## Features

- **Authentication**: Setup with Amazon Cognito for secure user authentication with Thai Localization 🇹🇭
- **API**: Ready-to-use GraphQL endpoint with AWS AppSync.
- **Database**: Real-time database powered by Amazon DynamoDB.



## License

This library is licensed under the MIT-0 License. See the LICENSE file.

## QuickStart
1. Clone or download this repository. 

2. Install all the project dependencies
```bash
npm install
```
3. Start local sandbox. It's required a configured AWS cli environment, the procedure will guide to setup if not available.
```bash
npx ampx sandbox
```

4. Run locally
```bash
npx run dev
```

5. Deploying to AWS
For detailed instructions on deploying your application, refer to the [deployment section](https://docs.amplify.aws/vue/start/quickstart/#deploy-a-fullstack-app-to-aws) of AWS documentation from Step 2.