---
title: โอนย้ายสินทรัพย์ถาวร
description: คู่มืองานนี้จะโอนข้อมูลทางการเงินสำหรับสมุดบัญชีสินทรัพย์ถาวรจากหนึ่งชุดมิติทางการเงินเพื่อตั้งค่ามิติทางการเงินใหม่
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c8428467d6e12b6d6af9023980b8cf8738d9294
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727018"
---
# <a name="transfer-a-fixed-asset"></a>โอนย้ายสินทรัพย์ถาวร

[!include [banner](../../includes/banner.md)]

คู่มืองานนี้จะโอนข้อมูลทางการเงินสำหรับสมุดบัญชีสินทรัพย์ถาวรจากหนึ่งชุดมิติทางการเงินเพื่อตั้งค่ามิติทางการเงินใหม่  

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**
2. ในรายการ ค้นหาและเลือกสินทรัพย์ถาวรที่จะโอน
3. ในบานหน้าต่างการดำเนินการ คลิก **สินทรัพย์ถาวร**
4. คลิก **โอนย้ายสินทรัพย์ถาวร**
5. ในฟิลด์ **วันที่โอนย้าย** ให้ป้อนวันที่
6. ป้อนข้อคิดเห็นที่อธิบายการโอน
    
    รายการนี้แสดงสมุดบัญชีทั้งหมดสำหรับสินทรัพย์ถาวร  
7. ทำเครื่องหมายสมุดบัญชีที่คุณต้องการโอนไปยังชุดมิติทางการเงินใหม่
    * รายการนี้แสดงค่ามิติทางการเงินที่มีอยู่สำหรับสมุดบัญชีที่เลือก  
    * เลือกมิติทางการเงินที่คุณต้องการอัปเดตสำหรับสมุดบัญชีสินทรัพย์ถาวรที่เลือก  
8. ในฟิลด์ **มิติทางการเงิน** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * ตั้งค่ามิติทางการเงินอื่นๆ ตามความเหมาะสม  
    * ทุกค่ามิติทางการเงินจะเปลี่ยนไปเมื่อมีการโอนเกิดขึ้น ไม่ว่าจะเป็นค่าที่ได้รับการป้อนหรือเว้นว่าง  ในตัวอย่าง ถ้าคุณป้อนค่าสำหรับหน่วยธุรกิจและปล่อยศูนย์ต้นทุนและแผนกมิติทางการเงินให้ว่างไว้ ถ้าโครงสร้างทางบัญชีของคุณอนุญาตให้มีค่าว่างเปล่าสำหรับศูนย์ต้นทุนและแผนก การโอนจะส่งผลให้แต่ละรูปแบบมูลค่ามีค่าใหม่สำหรับหน่วยธุรกิจและค่าว่างสำหรับศูนย์ต้นทุนและแผนก  
9. คลิก **อัปเดต** ข้อมูลเพิ่มเติมจะแสดงขึ้น
    * คุณมีโอกาสที่จะแสดงตัวอย่างการเปลี่ยนแปลงก่อนที่จะเสร็จสิ้นการโอน  
    * ตรวจทานผลลัพธ์ก่อนที่จะมีการโอนสมุดบัญชีสินทรัพย์ถาวร  
10. คลิก **โอนย้าย** 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
