---
title: ตั้งค่าคอนฟิกร้านค้าออนไลน์
description: บทความนี้แสดงลิงค์ไปยังหัวข้อที่จะช่วยให้คุณในการตั้งค่าคอนฟิกและจัดการจากส่วนกลางและร้านค้าออนไลน์
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 551a0a1e524f4aa30b2420e6ec384c92f48e95ae
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683395"
---
# <a name="configure-online-stores"></a>ตั้งค่าคอนฟิกร้านค้าออนไลน์

[!include [banner](../includes/banner.md)]

บทความนี้แสดงลิงค์ไปยังหัวข้อที่จะช่วยให้คุณในการตั้งค่าคอนฟิกและจัดการจากส่วนกลางและร้านค้าออนไลน์

หัวข้อที่แสดงรายการอยู่ในตารางต่อไปนี้ช่วยคุณในการตั้งค่าคอนฟิกส่วนประกอบ Commerce และร้านค้าปลีกออนไลน์ในไคลเอนต์

## <a name="configure-an-online-store"></a>ตั้งค่าคอนฟิกร้านค้าออนไลน์

| งาน                                                | รายละเอียด                                                                                                                                                                                                                                                                                                                                                   | เบ็ดเตล็ด                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ตั้งค่าคอนฟิกส่วนประกอบ                        | ตั้งค่าและรักษาข้อมูลสำหรับการดำเนินงานการค้า ข้อมูลนี้รวมถึงร้านค้า ภาษี ผลิตภัณฑ์ บัตรของขวัญ โปรโมชัน และส่วนลด                                                                                                                                                                                                          | [การตั้งค่าและการรักษาการขายปลีก](https://technet.microsoft.com/library/hh597201.aspx) (เนื้อหา TechNet สำหรับ Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                          |
| ตั้งค่าคอนฟิกลำดับชั้นการนำทางของช่องทาง    | สร้างลำดับชั้นของประเภทการนำทางในช่องทางเพื่อตั้งค่าโครงสร้างประเภทสำหรับผลิตภัณฑ์ที่คุณเสนอผ่านร้านค้าออนไลน์ ให้คุณกำหนดการจัดประเภทตามลำดับชั้น และกำหนดผลิตภัณฑ์ กลุ่มคุณลักษณะของผลิตภัณฑ์ และค่าแอททริบิวต์ให้กับประเภท จากนั้นให้คุณกำหนดการจัดประเภทตามลำดับชั้นไปยังร้านค้าออนไลน์                            | [ตั้งค่าลำดับชั้นการขายปลีก](https://technet.microsoft.com/library/hh580593.aspx)</br> (เนื้อหา TechNet สำหรับ AX 2012)</br> [ตั้งค่าแอตทริบิวต์และชนิดของแอตทริบิวต์](https://technet.microsoft.com/library/hh227548.aspx) (เนื้อหา TechNet สำหรับ AX 2012)</br> [ตั้งค่ากลุ่มแอตทริบิวต์การขายปลีก](https://technet.microsoft.com/library/jj728713.aspx) (เนื้อหา TechNet สำหรับ AX 2012) |
| เพิ่มร้านค้าออนไลน์ลงในลำดับชั้นขององค์กร | ก่อนที่คุณสามารถกำหนดให้การจัดประเภทผลิตภัณฑ์ หรือให้ตอบสนองใบสั่งสำหรับร้านค้าออนไลน์ที่คุณสร้างขึ้น หรือสร้างรายงานที่รวมข้อมูลจากร้านค้าออนไลน์นั้น จากนั้นคุณต้องกำหนดร้านค้าให้ลำดับชั้นขององค์กรหนึ่งรายการขึ้นไป อย่างน้อยที่สุด คุณต้องกำหนดร้านค้าออนไลน์ให้ลำดับชั้นขององค์กรที่มีการจัดประเภทผลิตภัณฑ์  | [ตั้งค่าร้านค้าออนไลน์](https://technet.microsoft.com/library/jj682095.aspx) (เนื้อหา TechNet สำหรับ AX 2012)                                                                                                                                                                                                                                                                                                     |
| เพิ่มวิธีการจัดส่งลงในร้านค้าออนไลน์          | เลือกวิธีการจัดส่งที่ร้านค้าออนไลน์มี                                                                                                                                                                                                                                                                                                 | [ตั้งค่าร้านค้าออนไลน์](https://technet.microsoft.com/library/jj682095.aspx) (เนื้อหา TechNet สำหรับ Microsoft AX 2012)                                                                                                                                                                                                                                                                                                     |
| แม็ปแอททริบิวต์และเพิ่มข้อมูลเมตา                   | เลือกตัวเลือกที่ระบุวิธีที่แอททริบิวต์ของแต่ละประเภทหรือผลิตภัณฑ์ในช่องทางควรเป็นในร้านค้าออนไลน์บนไซต์ Microsoft SharePoint                                                                                                                                                                                              | [ตั้งค่าร้านค้าออนไลน์](https://technet.microsoft.com/library/jj682095.aspx) (เนื้อหา TechNet สำหรับ AX 2012)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>ตั้งค่าคอนฟิกผลิตภัณฑ์ของร้านค้าออนไลน์

| งาน                                 | รายละเอียด                                                                                                                                           | เบ็ดเตล็ด                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| เพิ่มการจัดประเภทลงในร้านค้าออนไลน์ | เพิ่มการจัดประเภทที่รวมผลิตภัณฑ์ที่คุณเสนอในร้านค้าออนไลน์                                                                  | [ตั้งค่าร้านค้าออนไลน์](https://technet.microsoft.com/library/jj682095.aspx) (เนื้อหา TechNet สำหรับ AX 2012)                                                                                                                                              |
| จัดการแค็ตตาล็อก                     | ใช้แค็ตตาล็อกผลิตภัณฑ์เพื่อระบุผลิตภัณฑ์ที่คุณต้องการนำเสนอในร้านค้าของคุณ                                                              | [งานหลัก: สร้างแค็ตตาล็อกผลิตภัณฑ์ขายปลีก](https://technet.microsoft.com/library/jj728712.aspx) (เนื้อหา TechNet สำหรับ AX 2012)                                                                                                                           |
| จัดการราคา                       | ตั้งค่าและใช้กลุ่มราคาซึ่งเป็นการเชื่อมโยงศูนย์กลางระหว่างราคาและส่วนลด และช่องทาง แค็ตตาล็อก สังกัด และโปรแกรมตอบแทนลูกค้าสมาชิก | [การตั้งค่าราคาโดยใช้กลุ่มราคา](https://technet.microsoft.com/library/hh597169.aspx) (เนื้อหา TechNet สำหรับ AX 2012)</br> [การตั้งค่าภาษี](https://technet.microsoft.com/library/hh580571.aspx) (เนื้อหา TechNet AX สำหรับ 2012) |
| จัดการส่วนลด                    | ตั้งค่าและจัดการการปรับปรุงราคาและส่วนลดสี่ชนิด                                                                                  | [การตั้งค่าการปรับปรุงราคาและส่วนลด](https://technet.microsoft.com/library/hh597114.aspx) (เนื้อหา TechNet สำหรับ AX 2012)                                                                                                                          |
| จัดการค่าธรรมเนียมการจัดส่ง             | ตั้งค่าและจัดการค่าธรรมเนียมการจัดส่งที่เกี่ยวข้องเฉพาะกับร้านค้าออนไลน์                                                                     | [ตั้งค่าค่าธรรมเนียมการจัดส่งสำหรับร้านค้าออนไลน์](https://technet.microsoft.com/library/jj728714.aspx) (เนื้อหา TechNet สำหรับ AX 2012)                                                                                                                           |
| จัดการวิธีการจัดส่ง            | จัดการวิธีการจัดส่งที่ร้านค้าออนไลน์มี                                                                                        | [ตั้งค่าวิธีการจัดส่ง](https://technet.microsoft.com/library/jj728719.aspx) (เนื้อหา TechNet สำหรับ AX 2012)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>ตั้งค่าการแลกเปลี่ยนข้อมูลระหว่าง Commerce และร้านค้าออนไลน์

| งาน                                 | รายละเอียด                                                                                                                               | เบ็ดเตล็ด                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ตั้งค่าโพรไฟล์การรวมช่องทาง | โปรไฟล์ทำให้ส่วนประกอบสามารถสื่อสารกันได้ ตั้งค่าโพรไฟล์ก่อนที่คุณจะตั้งค่าคอนฟิกการตั้งค่าการแลกเปลี่ยนข้อมูล | [ตั้งค่าโปรไฟล์บริการแบบเรียลไทม์](https://technet.microsoft.com/library/hh580631.aspx) (เนื้อหา TechNet AX สำหรับ 2012)</br> [ตั้งค่าโปรไฟล์ช่องทาง](https://technet.microsoft.com/library/jj677402.aspx) (เนื้อหา TechNet AX สำหรับ 2012) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]