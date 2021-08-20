---
title: ชนิดการชำระเงินต้องเป็นข้อผิดพลาดเกี่ยวกับบัตรเครดิตในหน้าใบสั่งขาย
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการแสดงข้อความแสดงข้อผิดพลาดบนหน้าใบสั่งขายหลังจากการซิงค์ใบสั่งแล้ว
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
ms.openlocfilehash: 03bcbedb12b95a00141d27e9a93186a7fa7dabba70147177524f604dd10ed252
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750683"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>"ชนิดการชำระเงินต้องเป็นข้อผิดพลาดเกี่ยวกับบัตรเครดิต" ในหน้าใบสั่งขาย

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการแสดงข้อความแสดงข้อผิดพลาดบนหน้าใบสั่งขายหลังจากการซิงค์ใบสั่งแล้ว

## <a name="description"></a>คำอธิบาย

เมื่อคุณเปิดหน้าใบสั่งขายหลังจากที่คุณซิงค์ใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ชนิดการชำระเงินต้องเป็นบัตรเครดิต เนื่องจากมีการระบุหมายเลขบัตรเครดิตแล้ว"

![ข้อผิดพลาดชนิดการชำระเงินต้องเป็นบัตรเครดิต](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>การแก้ปัญหา

### <a name="set-the-payment-type-in-commerce-headquarters"></a>ตั้งค่าชนิดการชำระเงินในศูนย์ควบคุม Commerce

1. ไปที่ **บัญชีลูกหนี้ \> การตั้งค่าการชำระเงิน \> เงื่อนไขการชำระเงิน**
1. ในการนําทางด้านซ้าย ให้เลือกเงื่อนไขการชำระเงินของคุณ
1. ในฟิลด์ **ชนิดการชำระเงิน** ให้ตรวจสอบให้แน่ใจว่ามีการเลือก **บัตรเครดิต** แล้ว

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การลงรายการบัญชีการขายออนไลน์และการชำระเงิน](../tasks/posting-online-sales-payments.md)
