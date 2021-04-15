---
title: ครอบตัดรูปภาพ
description: หัวข้อนี้อธิบายวิธีการครอบตัดภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b90199e2f6c22863c379b488e8d89c566a14ec9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799336"
---
# <a name="crop-images"></a>ครอบตัดรูปภาพ

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการครอบตัดภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce

ไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce จะช่วยให้คุณสามารถตัดรูปเพื่อให้เหมาะสมกับชนิดโมดูลและ viewports ต่างๆ

## <a name="crop-an-image"></a>ตัดรูปภาพ

เมื่อต้องการตัดรูปภาพในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างนำทางด้านซ้ายของโปรแกรมสร้างไซต์ Commerce ให้เลือก **ไลบรารีสื่อ**
1. ในหน้าต่างหลัก เลือกภาพที่คุณต้องการแก้ไข
1. บนแถบคำสั่ง ให้เลือก **แก้ไข**
1. เลือกรูปภาพเพื่อป้อน **โหมดแก้ไข**
1. ภายใต้ **โหมดแก้ไข** เลือก **แก้ไขมุมมองตามโมดูล**
1. จากเมนูแบบหล่นลง **โมดูล** เลือกชนิดโมดูล
1. จากเมนูแบบหล่นลง **ชนิดมุมมอง** เลือกชนิดมุมมอง
1. จากเมนูแบบหล่นลง **การจัดวาง** เลือกการจัดวางภาพ
1. จากเมนูแบบหล่นลง **ช่องมุมมอง** เลือกขนาดช่องมุมมอง
1. ภาพถูกวางทับกับพื้นที่ซึ่งแสดงถึงเขตการตัด ย้ายและปรับขนาดเขตการตัดตามต้องการ อัตราส่วนกว้างยาวจะถูกเก็บรักษาไว้โดยอัตโนมัติ
1. เมื่อคุณดำเนินการเสร็จสิ้นแล้ว บนแถบคำสั่ง ให้เลือก **บันทึก** และจากนั้น เลือก **เสร็จสิ้นการแก้ไข** 

หลังจากการตัดแบบกำหนดเองเสร็จสมบูรณ์แล้ว การปรับเปลี่ยนรูปภาพจะมีผลเกือบทันที

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการจัดการสินทรัพย์ดิจิทัล](dam-overview.md)

[อัพโหลดรูปภาพ](dam-upload-images.md)

[อัพโหลดวิดีโอ](dam-upload-video.md)

[อัพโหลดไฟล์](dam-upload-files.md)

[ปรับแต่งจุดโฟกัสของรูปภาพ](dam-custom-focal-point.md)

[อัปโหลดและให้บริการไฟล์แบบคงที่](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
