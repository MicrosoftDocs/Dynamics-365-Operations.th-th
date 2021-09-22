---
title: จำนวนของทศนิยมสูงสุดสำหรับหน่วยการเก็บสต็อกสินค้าคือ 0
description: เมื่อคุณพยายามลงรายการบัญชีธุรกรรมสินค้าคงคลังหรือการจองสินค้าคงคลัง คุณจะได้รับข้อผิดพลาด "จํานวนทศนิยมสูงสุดสำหรับหน่วยการเก็บสต็อกสินค้าคือ 0"
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477779"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>จำนวนของทศนิยมสูงสุดสำหรับหน่วยการเก็บสต็อกสินค้าคือ 0


## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามลงรายการบัญชีธุรกรรมสินค้าคงคลังหรือการจองสินค้าคงคลัง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> จำนวนของทศนิยมสูงสุดสำหรับหน่วยการเก็บสต็อกสินค้าคือ 0

ปัญหานี้จะเกิดขึ้นเมื่อปริมาณรายการความเคลื่อนไหวของสินค้าคงคลังถูกระบุเป็นค่าทศนิยมที่ตด้านล่างระดับความแน่นอนที่ฟิลด์นี้สนับสนุน ตัวอย่างเช่น มีการระบุปริมาณเป็น *0.5* สำหรับธุรกรรมสินค้าคงคลัง แต่มีการสนับสนุนเฉพาะปริมาณจํานวนเต็มเท่านั้น ดังนั้น ค่าควรเป็น *1* แทน *0.5*

## <a name="resolution"></a>การแก้ปัญหา

1. รันสคริปต์ต่อไปนี้บนอินสแตนซ์ SQL Server ของคุณเพื่อปัดเศษปริมาณในธุรกรรมสินค้าคงคลัง สคริปต์นี้จะแก้ไขค่าในตาราง **inventTrans**

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. รันการตรวจสอบความสอดคล้องกันของปริมาณคงเหลือเมื่อตัวเลือก **แก้ไขข้อผิดพลาด** เปิดอยู่ การตรวจสอบนี้จะแก้ไขค่าในตาราง **inventSum**

> [!IMPORTANT]
> เราขอแนะนาเป็นอย่างยิ่งให้คุณแก้ไขสคริปต์อย่างถี่ถ้วนตามความต้องการของสภาพแวดล้อมของคุณ ทดสอบสคริปต์ในสภาพแวดล้อมการทดสอบ แล้วตรวจสอบข้อมูลที่เป็นผลลัพธ์ก่อนที่คุณจะรันสคริปต์ในสภาพแวดล้อมการผลิต
