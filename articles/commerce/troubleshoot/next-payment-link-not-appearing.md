---
title: ไม่ปรากฏตัวเลือกบันทึกการชำระเงินถัดไปของฉัน
description: หัวข้อนี้แสดงการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเมื่อกล่องกาเครื่องหมาย บันทึกสําหรับการชำระเงินถัดไปของฉัน ไม่ปรากฏขึ้นภายใต้วิธีการจ่ายเงินในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซ
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018445"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>ไม่ปรากฏตัวเลือก "บันทึกการชำระเงินถัดไปของฉัน"

[!include [banner](../../includes/banner.md)]

หัวข้อนี้แสดงการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเมื่อกล่องกาเครื่องหมาย  **บันทึกสําหรับการชำระเงินถัดไปของฉัน** ไม่ปรากฏขึ้นภายใต้ **วิธีการจ่ายเงิน** ในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซ

## <a name="description"></a>คำอธิบาย

กล่องกาเครื่องหมาย  **บันทึกสำหรับการชำระเงินครั้งถัดไปของฉัน** ไม่ปรากฏในส่วน **วิธีการชำระเงิน** ในหน้าเช็คเอาท์ของไซต์อีคอมเมิร์ซ

รูปภาพประกอบต่อไปนี้จะแสดงตัวอย่างของหน้าเช็คเอาท์ที่รวมกล่องกาเครื่องหมาย **บันทึกสำหรับการชำระเงินครั้งถัดไปของฉัน**

![กล่องกาเครื่องหมายบันทึกสำหรับการชำระเงินครั้งถัดไปของฉันในโมดูลการชำระเงิน](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>ความละเอียด

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>ตรวจสอบว่า Dynamics 365 Payment Connector สำหรับ Adyen ได้รับการตั้งค่าคอนฟิกอย่างถูกต้องในศูนย์ควบคุม Commerce

ให้ทำตามขั้นตอนดังต่อไปนี้ เพื่อตรวจสอบว่า Dynamics 365 Payment Connector สำหรับ Adyen ได้รับการตั้งค่าคอนฟิกอย่างถูกต้องในศูนย์ควบคุม Commerce 

1. ไปที่การ **Retail และ Commerce \> ช่องทาง \>ร้านค้าออนไลน์**
1. เลือกร้านค้าออนไลน์
1. บนแท็บด่วน **บัญชีการชำระเงิน** ตรวจสอบให้แน่ใจว่าได้ตั้งค่าฟิลด์ **อนุญาตให้บันทึกข้อมูลการชำระเงินในอีคอมเมิร์ซ** เป็น **จริง**

![อนุญาตให้บันทึกข้อมูลการชำระเงินในฟิลด์อีคอมเมิร์ซในศูนย์ควบคุม Commerce](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[โมดูลการชำระเงิน](../payment-module.md)

[การบันทึกเครื่องมือการชำระเงินออนไลน์ด้วยตัวเชื่อมต่อ Adyen](../dev-itpro/adyen-connector-listPI.md)
