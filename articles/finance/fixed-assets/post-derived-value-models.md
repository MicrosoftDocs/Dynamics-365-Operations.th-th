---
title: ลงรายการบัญชีด้วยสมุดบัญชีที่ได้รับ
description: บทความนี้อธิบายวิธีการใช้สมุดบัญชี
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0270ad1e66193832fb1139fca4439b36b5ffb84
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682919"
---
# <a name="post-with-derived-books"></a>ลงรายการบัญชีด้วยสมุดบัญชีที่ได้รับ

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการใช้สมุดบัญชี

เมื่อคุณลงรายบัญชีธุรกรรมสำหรับสมุดบัญชีที่ประกอบด้วยสมุดบัญชีที่ได้รับ ธุรกรรมสมุดบัญชีที่ได้รับนี้จะมีการลงรายการบัญชีโดยอัตโนมัติในสมุดรายวัน ใบสั่งซื้อ หรือใบแจ้งหนี้ข้อความอิสระ อย่างไรก็ตาม ถ้าคุณจัดเตรียมธุรกรรมสมุดบัญชีหลักในสมุดรายวันสินทรัพย์ถาวร คุณสามารถดูและแก้ไขยอดเงินของธุรกรรมที่ได้รับก่อนที่จะลงรายการบัญชีธุรกรรมเหล่านั้น
-   บัญชีบางบัญชี เช่น บัญชีภาษีขายและบัญชีลูกค้าหรือผู้จัดจำหน่าย จะถูกอัพเดตเพียงครั้งเดียวด้วยการลงรายการบัญชีสมุดบัญชีหลัก ธุรกรรมสมุดบัญชีที่ได้รับจะมีการลงรายการบัญชีไปยังบัญชีที่กำหนดไว้สำหรับสมุดบัญชีที่ได้รับในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร
-   การซื้อสินทรัพย์มักใช้เป็นชนิดธุรกรรมสำหรับสมุดบัญชีที่ได้รับ คุณจะใช้ธุรกรรมชนิดนี้เมื่อใช้สมุดบัญชีและสมุดบัญชีค่าเสื่อมราคาที่ได้รับกับสินทรัพย์ถาวรตั้งแต่เมื่อซื้อสินทรัพย์ถาวรนั้นมา
-   มูลค่าอื่นๆ สำหรับชนิดธุรกรรมสามารถใช้ได้เช่นกัน นอกจากนี้ คุณสามารถใช้ค่าอื่นๆ สำหรับชนิดธุรกรรมได้เช่นกัน ตัวอย่างเช่น ถ้าสมุดบัญชีหลักและสมุดบัญชีที่ได้รับอยู่ในช่วงเดียวกัน ซึ่งเกี่ยวข้องกับการขายหรือการตัดจำหน่าย ชนิดธุรกรรมสินทรัพย์ถาวรทั้งหมดจะพร้อมใช้งานสำหรับการตั้งค่าสมุดบัญชีค่าเสื่อมราคาที่ได้รับ

> [!WARNING]
> ค่าเสื่อมราคาที่ลงรายการบัญชีในสมุดบัญชีที่ได้รับจะเป็นจำนวนยอดเงินเดียวกันกับที่ลงรายการบัญชีไว้สำหรับสมุดบัญชีหลัก ถ้าวิธีการคิดค่าเสื่อมราคาแตกต่างกันระหว่างสมุดบัญชีต่างๆ คุณไม่ควรสร้างธุรกรรมค่าเสื่อมราคาโดยใช้กระบวนการที่ได้รับ 

## <a name="example"></a>ตัวอย่าง 
ข้อมูลต่อไปนี้อธิบายวิธีการตั้งค่าธุรกรรมการซื้อด้วยฟังก์ชันสมุดบัญชีที่ได้รับ

1.  สร้างสมุดบัญชีบนหน้าสมุดบัญชี
    -   สมุดบัญชีสำหรับการลงบัญชี: VM 1 ชั้นการลงรายการบัญชีปัจจุบัน
    -   สมุดบัญชีสำหรับวัตถุประสงค์ด้านภาษี: VM 2 ชั้นของการลงรายการบัญชีภาษี

2.  บน VM 1 คลิกแท็บสมุดบัญชีที่ได้รับมา และเลือก VM 2 ในฟิลด์สมุดบัญชี และการซื้อสินทรัพย์ในฟิลด์ชนิดธุรกรรม

จากนั้น ก็สามารถแนบสมุดบัญชีกับสินทรัพย์ถาวรที่เฉพาะเจาะจงได้ 

เมื่อมีการลงรายการบัญชีการซื้อสำหรับสินทรัพย์ถาวรที่มีสมุดบัญชี VM 1 จะมีการลงรายการบัญชีการซื้อไม่เพียงแต่ใน VM 1 เท่านั้น แต่ยังลงบัญชีในสมุดบัญชีที่ได้รับ VM 2 อีกด้วย สถานะของสมุดบัญชีสินทรัพย์ถาวรทั้งสองจะถูกอัพเดตเป็นเปิด

> [!NOTE]                                                                                                         
> ถ้าคุณไม่ใช้สมุดบัญชีที่ได้รับ คุณต้องลงรายการบัญชีการซื้อสินทรัพย์ถาวรทั้งสำหรับสมุดบัญชี VM 1 และสมุดบัญชี VM 2

สำหรับข้อมูลเพิ่มเติม ดู [สมุดบัญชีที่ได้รับ](derived-books.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
