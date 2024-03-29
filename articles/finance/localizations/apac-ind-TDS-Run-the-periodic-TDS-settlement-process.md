---
title: รันกระบวนการชําระเงิน TDS ประจำงวด
description: บทความนี้อธิบายวิธีการชำระภาษีที่หักที่ต้นทาง (TDS) ประจำงวด
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1376e2ae342aedb8fe44d95a11dd47f906a4ca48
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864255"
---
# <a name="run-the-periodic-tds-settlement-process"></a>รันกระบวนการชําระเงิน TDS ประจำงวด

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการชำระภาษีที่หักที่ต้นทาง (TDS) ประจำงวด

1. ไปที่ **ภาษี \> ประกาศต่างๆ \> ภาษีหัก ณ ที่จ่าย \> การชำระภาษีหัก ณ ที่จ่าย**

    [![กล่องโต้ตอบการชำระภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. ในกล่องโต้ตอบ **การชำระภาษีหัก ณ ที่จ่าย** ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS**
3. ในฟิลด์ **หมายเลขบัญชีภาษี (TAN)** ให้เลือกหมายเลขบัญชีภาษี (TAN) ที่จะรันกระบวนการเดอะเซตเทิลเมนต์ให้
4. ในฟิลด์ **กลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย** ให้เลือกกลุ่มส่วนประกอบ TDS ที่จะรันกระบวนการเดอะเซตเทิลเมนต์ให้
5. ในฟิลด์ **รอบระยะเวลาการชําระเงิน** เลือกรอบระยะเวลาการชําระเงิน TDS เพื่อรันกระบวนการเดอะเซตเทิลเมนต์ให้

    > [!NOTE]
    > กระบวนการชําระเงิน TDS ถูกรันสำหรับรอบระยะเวลาทั้งหมดที่ตั้งค่าไว้สำหรับรอบระยะเวลาการชําระภาษีหัก ณ ที่จ่ายบนแท็บ **รอบระยะเวลา** ของหน้า **รอบระยะเวลาการชําระภาษีหัก ณ ที่จ่าย** (**ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> รอบระยะเวลาการชําระภาษีหัก ณ ที่จ่าย**)

6. ในฟิลด์ **วันที่เริ่มต้น** ให้เลือกวันที่เริ่มต้นที่จะรันกระบวนการชําระเงิน TDS

    สำหรับรอบระยะเวลาเฉพาะภายในรอบระยะเวลาเดอะเซตเทิลเมนต์ วันที่เริ่มต้นที่กําหนดไว้สำหรับรอบระยะเวลาจะถูกใช้เป็นวันที่ "เริ่มต้น" ตัวอย่างเช่น รอบระยะเวลาการชำระเงิน TDS มีสองรอบระยะเวลา: 1 เมษายน ถึง 30 เมษายน 2009 และ 1 พฤษภาคม ถึง 31 พฤษภาคม 2009 ถ้าคุณเลือก **04/06/2009** (6 เมษายน 2009) เป็นวันที่เริ่มต้นในฟิลด์ **วันที่เริ่มต้น** กระบวนการชําระเงินจะยังคงรันตั้งแต่วันที่ 1 เมษายน 2009

    ถ้าคุณป้อนรอบระยะเวลาในภายหลังในฟิลด์ **วันที่เริ่มต้น** แต่ไม่มีการชําระเงินรอบระยะเวลาก่อนหน้านี้ภายในรอบระยะเวลาเดอะเซตเทิลเมนต์ เดอะเซตเทิลเมนต์จะไม่เกิดขึ้นสำหรับรอบระยะเวลาก่อนหน้าใดๆ ตัวอย่างเช่น รอบระยะเวลาการชําระเงิน TDS มีสามรอบระยะเวลา: 1 เมษายน ถึง 30 เมษายน 2009, วันที่ 1 พฤษภาคม ถึง 31 พฤษภาคม 2009 และ 1 มิถุนายนจนถึงวันที่ 30 มิถุนายน 2009 ถ้าคุณเลือก **05/01/2009** (1 พฤษภาคม 2009) เป็นวันที่เริ่มต้นในฟิลด์ **วันที่เริ่มต้น** กระบวนการเดอะเซตเทิลเมนต์จะรันได้ตั้งแต่ 1 พฤษภาคมจนถึง วันที่ 31 พฤษภาคม 2009 เท่านั้น เดอะเซตเทิลเมนต์จะไม่เกิดขึ้นสำหรับวันที่ 1 เมษายน ถึง 30 เมษายน 2009

7. ในฟิลด์ **วันที่ธุรกรรม** ให้เลือกวันที่ที่จะลงรายการบัญชีธุรกรรมการชําระเงิน TDS
8. ในฟิลด์ **เวอร์ชันการชำระภาษีหัก ณ ที่จ่าย** ให้เลือกเวอร์ชันการชำระเงิน TDS:

     - **ดั้งเดิม** – ใช้ตัวเลือกนี้เพื่อรันกระบวนการชําระเงิน TDS เป็นครั้งแรก เวอร์ชันการชําระเงินดั้งเดิมจะถูกใช้เพียงครั้งหนึ่งในการรันกระบวนการชําระเงิน TDS สำหรับชุดของ TAN, กลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย และรอบระยะเวลาการชําระภาษีหัก ณ ที่จ่าย
    - **เวอร์ชันล่าสุด** – ใช้ตัวเลือกนี้ ถ้ามีการรันกระบวนการชําระเงิน TDS อยู่แล้วในรอบระยะเวลาที่ระบุ รวมธุรกรรมที่มีวันที่ย้อนหลังที่ถูกลงรายการบัญชีหลังจากรันกระบวนการเดอะเซตเทิลเมนต์ก่อนหน้านี้สำหรับรอบระยะเวลา คุณสามารถใช้ตัวเลือกนี้เพื่อรันกระบวนการเดอะเซตเทิลเมนต์หลายครั้ง

9. เลือกกล่องกาเครื่องหมาย **อัพเดต** เพื่อรันกระบวนการชําระเงิน TDS และลงรายการบัญชียอดเงินในบัญชีแยกประเภท ถ้ายกเลิกการเลือกกล่องกาเครื่องหมายนี้ กระบวนการเดอะเซตเทิลเมนต์จะไม่ถูกรัน และจะไม่มีการสร้างรายการทางการเงิน
10. เลือก **ตกลง** เพื่อรันกระบวนการชําระเงิน TDS และสร้างรายงานการชําระภาษีหัก ณ ที่จ่าย สถานะของธุรกรรม TDS ที่รวมอยู่ในกระบวนการเดอะเซตเทิลเมนต์จะแสดงเป็น **ชําระแล้ว** บนหน้า **การชําระเงิน** (ให้ไปที่ **บัญชีเจ้าหนี้ \> การชําระเงิน \> สมุดรายวันการชําระเงินของผู้จัดจำหน่าย** เลือก **รายการ** เลือก **ฟังก์ชัน** แล้วจากนั้น เลือก **การชําระเงิน**)

### <a name="important-points"></a>จุดสําคัญ

- หากไม่ได้เลือกกลุ่มส่วนประกอบภาษีหัก ณ ที่จ่ายในระหว่างกระบวนการเดอะเซตเทิลเมนต์ เดอะเซตเทิลเมนต์จะเกิดขึ้นสำหรับกลุ่มส่วนประกอบภาษีหัก ณ ที่จ่ายทั้งหมดสำหรับ TAN และรอบระยะเวลาการชําระเงินที่เลือก มีการสร้างบรรทัดแยกต่างหากสำหรับกลุ่มส่วนประกอบภาษีหัก ณ ที่จ่ายแต่ละกลุ่มในหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้**
- กระบวนการชําระเงินเป็นไปตามประเภทของลักษณะผู้ถูกประเมินสำหรับระยะเวลาการชําระเงิน ธุรกรรมที่ประเภทของลักษณะผู้ถูกประเมินเป็น **บริษัท** ถูกชำระและถูกแสดงเป็นบรรทัดเดียวในหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้** ธุรกรรมที่ลักษณะผู้ถูกประเมินเป็นอย่างอื่นนอกเหนือจาก **บริษัท** ถูกชำระและถูกแสดงเป็นบรรทัดเดียวในหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้**
- วันที่ครบกําหนดของรายการธุรกรรม TDS ที่ชำระแล้วในหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้** ขึ้นอยู่กับเงื่อนไขการชำระเงินที่กําหนดไว้สำหรับผู้จัดจำหน่ายของหน่วยงาน TDS ในหน้า **ผู้จัดจำหน่าย** ถ้าไม่ได้กําหนดเงื่อนไขการชําระเงินไว้สำหรับผู้จัดจำหน่ายของหน่วยงาน TDS วันสุดท้ายของรอบระยะเวลาเดอะเซตเทิลเมนต์จะแสดงเป็นวันที่ครบกําหนดชําระ
