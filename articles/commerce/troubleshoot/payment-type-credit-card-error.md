---
title: ชนิดการชำระเงินต้องเป็นข้อผิดพลาดเกี่ยวกับบัตรเครดิตในหน้าใบสั่งขาย
description: บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการแสดงข้อความแสดงข้อผิดพลาดบนหน้าใบสั่งขายหลังจากการซิงค์ใบสั่งแล้ว
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
ms.openlocfilehash: 794317a84a8a0ff205ac1b6a5caa6ef1cf098ea3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905354"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>"ชนิดการชำระเงินต้องเป็นข้อผิดพลาดเกี่ยวกับบัตรเครดิต" ในหน้าใบสั่งขาย

[!include [banner](../../includes/banner.md)]

บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยในการแสดงข้อความแสดงข้อผิดพลาดบนหน้าใบสั่งขายหลังจากการซิงค์ใบสั่งแล้ว

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
