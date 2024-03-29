---
title: บันทึกหมายเลขใบรับรอง TDS ที่ได้รับคืน
description: บทความนี้อธิบายวิธีการใช้หน้าใบรับรองที่จะได้รับคืน เพื่อบันทึกหมายเลขและวันที่ใบรับรองของใบรับรองภาษี ณ ที่จ่าย (TDS) ที่ได้รับจากผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภทที่ระบุ
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
ms.openlocfilehash: 513412e292167795fad9d80b68e6e5e14dbd13c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853269"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>บันทึกหมายเลขใบรับรอง TDS ที่ได้รับคืน

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการใช้หน้า **ใบรับรองที่จะได้รับคืน** เพื่อบันทึกหมายเลขและวันที่ใบรับรองของใบรับรองภาษี ณ ที่จ่าย (TDS) ที่ได้รับจากผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภทที่ระบุ เมื่อต้องการอัปเดตหมายเลขและวันที่ในใบรับรอง TDS ที่บันทึกให้กับธุรกรรม TDS บนหน้านี้ ให้ใช้หน้า **อัปเดตใบรับรอง** (**บัญชีแยกประเภททั่วไป \> ประจำงวด \> ภาษีหัก ณ ที่จ่าย \> อัปเดตใบรับรอง**) หลังจากที่คุณอัปเดตหมายเลขใบรับรอง TDS เสร็จสิ้นแล้ว ให้ปิด

ปฏิบัติตามขั้นตอนเหล่านี้ เพื่อบันทึกหมายเลขและวันที่ใบรับรอง TDS

1. ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> ใบรับรองที่จะได้รับคืน**

    [![หน้าใบรับรองที่จะได้รับคืน](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. บนหน้า **ใบรับรองที่จะได้รับคืน** ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS**
3. เลือก **สร้าง** เพื่อสร้างเรกคอร์ด
4. ในฟิลด์ **หมายเลขใบรับรอง** ป้อนหมายเลขใบรับรอง TDS
5. ในฟิลด์ **ชนิดบัญชี** ให้เลือกชนิดของบัญชีที่จะรับใบรับรอง TDS ได้แก่ **ผู้จัดจำหน่าย** **ลูกค้า** หรือ **บัญชีแยกประเภท**
6. ในฟิลด์ **บัญชี** ให้เลือกหมายเลขบัญชีผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท ทั้งนี้ขึ้นอยู่กับชนิดบัญชีที่คุณเลือกไว้ ฟิลด์ **ชื่อ** จะแสดงชื่อของบัญชีผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท
7. ในฟิลด์ **จำนวนเงินที่รับรอง** ป้อนชื่จำนวนของใบรับรอง TDS
8. ในฟิลด์ **วันที่** ป้อนวันที่รับรองของหมายเลขใบรับรอง
9. เลือก **การสอบถาม** เพื่อเปิดหน้า **ธุรกรรมใบรับรอง** ซึ่งคุณสามารถดูธุรกรรม TDS ที่มีการอัปเดตหมายเลขและวันที่ใบรับรอง TDS คุณสามารถอัปเดตข้อมูลนี้ในหน้า **อัปเดตใบรับรอง** (**ภาษี \> ประกาศต่างๆ \> ภาษีหัก ณ ที่จ่าย \> อัปเดตใบรับรอง**)

    แท็บ **อับเดตใบรับรอง** แสดงข้อมูลต่อไปนี้ของธุรกรรม TDS แต่ละธุรกรรม:

    - **วันที่** – วันที่ลงรายการบัญชีของธุรกรรม
    - **ใบสำคัญ** – หมายเลขใบสำคัญของธุรกรรม TDS
    - **แหล่งที่มา** – โมดูลที่มีการสร้างธุรกรรม TDS
    - **บัญชี** – หมายเลขผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท ที่มีการสร้างธุรกรรม TDS ให้
    - **ชื่อ** – ชื่อผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท ที่มีการสร้างธุรกรรม TDS ให้
    - **จำนวน** – ยอดที่ TDS คำนวณได้จากยอดเงินใบแจ้งหนี้
    - **ยอดภาษี** – ยอดภาษี TDS ที่คํานวณได้สำหรับธุรกรรม
    - **วันที่ในใบรับรอง** – วันที่ในใบรับรอง TDS ที่ได้รับการอัปเดตแล้วของธุรกรรม TDS
    - **หมายเลขใบรับรอง** – หมายเลขใบรับรอง TDS ที่ได้รับการอัปเดตแล้วของธุรกรรม TDS

10. บนหน้า **ใบรับรองที่จะได้รับคืน** ให้เลือกกล่องกาเครื่องหมาย **ปิด** เพื่อปิดหมายเลขใบรับรอง TDS หลังจากที่คุณเสร็จสิ้นการอัปเดตหมายเลขใบรับรองให้กับธุรกรรม TDS บนหน้า **อัปเดตใบรับรอง**

    เมื่อต้องการเลือกกล่องกาเครื่องหมาย **ปิด** ให้กับเรกคอร์ดทั้งหมดในหน้า ให้เลือก **เลือกทั้งหมด**

    > [!NOTE]
    > หมายเลขใบรับรอง TDS ที่มีการเลือกกล่องกาเครื่องหมาย **ปิด** ไว้ ไม่มีอยู่ในหน้า **อัปเดตใบรับรอง**
