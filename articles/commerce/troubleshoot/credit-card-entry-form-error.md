---
title: หน้ารายการบัตรเครดิตแสดงข้อผิดพลาดขณะชำระเงิน
description: หัวข้อนี้ให้แนวทางแก้ไขปัญหาที่สามารถช่วยได้เมื่อไม่ได้โหลดส่วนวิธีการชำระเงินและแสดงข้อความแสดงข้อผิดพลาด
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
ms.openlocfilehash: 613eb2af626ca315a8bacb89fb348a5b14bd17b1717a90c99bcede66baef9040
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752398"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>หน้ารายการบัตรเครดิตแสดงข้อผิดพลาดขณะชำระเงิน

[!include [banner](../../includes/banner.md)]

หัวข้อนี้ให้แนวทางแก้ไขปัญหาที่สามารถช่วยได้เมื่อไม่ได้โหลดส่วน **วิธีการชำระเงิน** และแสดงข้อความแสดงข้อผิดพลาด

## <a name="description"></a>คำอธิบาย

เมื่อคุณเปิดหน้าชำระเงินของร้านค้าออนไลน์ส่วน  **วิธีการชำระเงิน** จะไม่ถูกโหลด และข้อความแสดงข้อผิดพลาดต่อไปนี้จะปรากฎขึ้น "มีบางอย่างผิดปกติ กรุณาลองใหม่อีกครั้งในภายหลัง"

![ข้อผิดพลาดของโมดูลการชำระเงิน](media/payment-module-error.jpg)

## <a name="resolution"></a>การแก้ปัญหา

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>รอให้แคช Commerce Scale Unit หมดอายุ

การตั้งค่าบริการชำระเงินในหน้าชำระเงินของร้านค้าออนไลน์จะถูกแคชบน Commerce Scale Unit และอาจใช้เวลาถึง 15 นาทีจึงจะปรากฏบนไซต์อีคอมเมิร์ซ การตั้งค่าบริการชำระเงินเหล่านี้รวมถึงการเปลี่ยนแปลงรหัสบัญชีผู้ขาย คีย์ Cloud API และการตั้งค่าการกำหนดค่าคอนฟิกต่างๆ ที่เกี่ยวข้องกับวิธีการชำระเงิน

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าช่องทางออนไลน์](../channel-setup-online.md)
