---
title: ผลิตภัณฑ์และประเภทขาดหายไปหลังจากการคัดลอกสภาพแวดล้อม
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทขาดหายไปหลังจากที่คัดลอกไซต์ระหว่างสภาพแวดล้อมหรือภายในสภาพแวดล้อมเดียวกัน
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
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585563"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>ผลิตภัณฑ์และประเภทขาดหายไปหลังจากการคัดลอกสภาพแวดล้อม

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทขาดหายไปหลังจากที่คัดลอกไซต์ระหว่างสภาพแวดล้อมหรือภายในสภาพแวดล้อมเดียวกัน

## <a name="description"></a>คำอธิบาย

หลังจากคัดลอกไซต์จากสภาพแวดล้อมหนึ่งไปยังอีกสภาพแวดล้อมหนึ่ง หรือในสภาพแวดล้อมเดียวกัน ผลิตภัณฑ์และประเภทขาดหายไปจากไซต์ ผลิตภัณฑ์และประเภทขาดหายไปจากหน้าร้านอีคอมเมิร์ซและจากแท็บ **ผลิตภัณฑ์** ในโปรแกรมสร้างไซต์ Commerce

## <a name="resolution"></a>ความละเอียด

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>แม็ปหมายเลขหน่วยปฏิบัติงานของช่องทางกับไซต์ที่คัดลอกใหม่ของโปรแกรมสร้างไซต์ Commerce

ในการแม็ปหมายเลขหน่วยปฏิบัติงาน (OUN) ของช่องทางกับไซต์ที่คัดลอกใหม่ของโปรแกรมสร้างไซต์ Commerce ทำตามขั้นตอนดังต่อไปนี้

1. เลือกไซต์ที่คัดลอกใหม่
1. ด้านล่าง **การตั้งค่าไซต์** เลือก **ช่องทาง**
1. ถัดจากชื่อช่องทาง ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เปลี่ยนช่องทางร้านค้าออนไลน์**
1. ในกล่องโต้ตอบ **เปลี่ยนช่องทางร้านค้าออนไลน์** เลือกช่องทางที่จะแม็ปไปยังไซต์ที่คัดลอกใหม่ แล้วเลือก **ตกลง**
1. เลือก **Save and publish**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์](../associate-site-online-store.md)
