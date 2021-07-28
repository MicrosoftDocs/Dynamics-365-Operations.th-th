---
title: ข้อผิดพลาดในการซิงโครไนส์ใบสั่งที่เกี่ยวข้องกับบริการจ่ายเงินเริ่มต้น
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยแก้ไขข้อผิดพลาดที่อาจเกิดขึ้นเมื่อซิงค์ใบสั่งออนไลน์
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
ms.openlocfilehash: 647060635813ad7e680ea88be76668818ff606d3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350365"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>ข้อผิดพลาดในการซิงโครไนส์ใบสั่งที่เกี่ยวข้องกับบริการจ่ายเงินเริ่มต้น

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยแก้ไขข้อผิดพลาดที่อาจเกิดขึ้นเมื่อซิงค์ใบสั่งออนไลน์

## <a name="description"></a>คำอธิบาย

เมื่อคุณซิงค์ใบสั่งออนไลน์ คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ต้องมีบริการจ่ายเงินเริ่มต้นเพื่อประมวลผลธุรกรรมบัตรเครดิต"

![ข้อผิดพลาดของบริการจ่ายเงินเริ่มต้นที่ขาดหายไป](media/default-payment-method-error.jpg)

## <a name="resolution"></a>การแก้ปัญหา

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>ยืนยันหรือตั้งค่าบริการจ่ายเงินเริ่มต้นในศูนย์ควบคุม Commerce

ในการยืนยันหรือตั้งค่าบริการจ่ายเงินเริ่มต้นในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **บัญชีลูกหนี้ \> การตั้งค่าการชำระเงิน \> บริการชำระเงิน**
1. ตรวจสอบให้แน่ใจว่าตัวเลือก **ตัวประมวลผลเริ่มต้นเริ่มต้นของบัตรเครดิตใหม่** ได้รับการตั้งค่าเป็น **ใช่** บริการการชำระเงินหนึ่งรายการ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การตั้งค่า การตรวจสอบ และการรวบรวมข้อมูลบัตรเครดิต](../../finance/accounts-receivable/credit-card-authorizations.md)