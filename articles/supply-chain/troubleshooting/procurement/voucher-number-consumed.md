---
title: หมายเลขใบสำคัญของใบรับสินค้าจะถูกใช้ ถึงแม้ว่าจะไม่ได้สร้างใบสำคัญ
description: มีการใช้หมายเลขใบสำคัญของใบรับสินค้า ถึงแม้ว่าจะไม่มีการสร้างใบสำคัญทางการเงินในระหว่างการรับสินค้า
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477734"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>หมายเลขใบสำคัญของใบรับสินค้าจะถูกใช้ ถึงแม้ว่าจะไม่ได้สร้างใบสำคัญ

## <a name="symptoms"></a>อาการ

มีการใช้หมายเลขใบสำคัญของใบรับสินค้าถึงแม้ว่าจะไม่มีการสร้างใบสำคัญทางการเงินในระหว่างการรับสินค้า

## <a name="resolution"></a>การแก้ปัญหา

ถ้ามีการตั้งค่าตัวเลือก **บันทึกหนี้สินค้างจ่ายของใบรับสินค้า** เป็น *ไม่มี* สำหรับกลุ่มแบบจำลองสินค้า จะไม่มีการลงรายการบัญชีในบัญชีแยกประเภททั่วไป อย่างไรก็ตามจะมีการบันทึกเหตุการณ์ทางกายภาพสำหรับวัตถุประสงค์ของการบัญชีในบัญชีแยกประเภทย่อย และเหตุการณ์นั้นต้องใช้หมายเลขใบสำคัญ หมายเลขใบสำคัญนี้คือหมายเลขใบสำคัญที่มีการอ้างอิงในรายการธุรกรรมของสินค้าคงคลัง

เราขอแนะนำให้คุณตั้งค่าตัวเลือก **บันทึกหนี้สินค้างจ่ายของใบรับสินค้า** เป็น *ใช่* ดังที่อธิบายไว้ในการลงรายการบัญชีบล็อกต่อไปนี้: [ลงรายการบัญชีค่าธรรมเนียมเบ็ดเตล็ดในเวลาของใบรับสินค้า](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)
