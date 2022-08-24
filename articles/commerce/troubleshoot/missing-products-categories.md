---
title: ผลิตภัณฑ์และประเภทขาดหายไปหลังจากการคัดลอกสภาพแวดล้อม
description: บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทขาดหายไปหลังจากที่คัดลอกไซต์ระหว่างสภาพแวดล้อมหรือภายในสภาพแวดล้อมเดียวกัน
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d8df3f4cca6a7aaad98ffb7f2d284211a4f9589b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277918"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>ผลิตภัณฑ์และประเภทขาดหายไปหลังจากการคัดลอกสภาพแวดล้อม

[!include [banner](../../includes/banner.md)]

บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทขาดหายไปหลังจากที่คัดลอกไซต์ระหว่างสภาพแวดล้อมหรือภายในสภาพแวดล้อมเดียวกัน

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
