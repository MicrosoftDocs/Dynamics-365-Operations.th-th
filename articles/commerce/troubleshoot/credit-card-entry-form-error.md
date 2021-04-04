---
title: หน้ารายการบัตรเครดิตแสดงข้อผิดพลาดขณะชำระเงิน
description: หัวข้อนี้ให้แนวทางแก้ไขปัญหาที่สามารถช่วยได้เมื่อไม่ได้โหลดส่วนวิธีการชำระเงินและแสดงข้อความแสดงข้อผิดพลาด
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585550"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>หน้ารายการบัตรเครดิตแสดงข้อผิดพลาดขณะชำระเงิน

[!include [banner](../../includes/banner.md)]

หัวข้อนี้ให้แนวทางแก้ไขปัญหาที่สามารถช่วยได้เมื่อไม่ได้โหลดส่วน **วิธีการชำระเงิน** และแสดงข้อความแสดงข้อผิดพลาด

## <a name="description"></a>คำอธิบาย

เมื่อคุณเปิดหน้าชำระเงินของร้านค้าออนไลน์ส่วน  **วิธีการชำระเงิน** จะไม่ถูกโหลด และข้อความแสดงข้อผิดพลาดต่อไปนี้จะปรากฎขึ้น "มีบางอย่างผิดปกติ กรุณาลองใหม่อีกครั้งในภายหลัง"

![ข้อผิดพลาดของโมดูลการชำระเงิน](media/payment-module-error.jpg)

## <a name="resolution"></a>ความละเอียด

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>รอให้แคช Commerce Scale Unit หมดอายุ

การตั้งค่าบริการชำระเงินในหน้าชำระเงินของร้านค้าออนไลน์จะถูกแคชบน Commerce Scale Unit และอาจใช้เวลาถึง 15 นาทีจึงจะปรากฏบนไซต์อีคอมเมิร์ซ การตั้งค่าบริการชำระเงินเหล่านี้รวมถึงการเปลี่ยนแปลงรหัสบัญชีผู้ขาย คีย์ Cloud API และการตั้งค่าการกำหนดค่าคอนฟิกต่างๆ ที่เกี่ยวข้องกับวิธีการชำระเงิน

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าช่องทางออนไลน์](../channel-setup-online.md)
