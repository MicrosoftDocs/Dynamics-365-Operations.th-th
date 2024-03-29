---
title: ภาพรวมของวัตถุที่ให้บริการ
description: บทความนี้แสดงภาพรวมวิธีการงานกับวัตถุที่ให้บริการ
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8150a94677fe38f4caa6f3e0b5fb5d1be5972eaf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862424"
---
# <a name="service-objects-overview"></a>ภาพรวมของวัตถุที่ให้บริการ

[!include [banner](../includes/banner.md)]

ออบเจ็กต์บริการคือสินทรัพย์ของลูกค้าและผลิตภัณฑ์ที่คุณสามารถใช้ดำเนินการให้บริการได้ วัตถุอาจเป็นสิ่งที่สามารถจับต้องได้หรือไม่ก็ได้ ทั้งนี้ขึ้นอยู่กับชนิดการบริการของคุณ

-  วัตถุที่สามารถจับต้องได้คือสิ่งที่เป็นรูปธรรม เช่น เครื่องจักรหรืออาคาร ซึ่งคุณสามารถใช้ดำเนินการภารกิจการให้บริการทางกายภาพ

    ออบเจ็กต์ที่ให้บริการแบบมีตัวตนยังอาจเป็นสินค้าในสินค้าคงคลังที่คุณสร้างไว้ในแบบฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้ คุณสามารถสร้างวัตถุที่ให้บริการได้จนถึงระดับข้อมูลที่มีหมายเลขลำดับประจำสินค้า ทั้งนี้ขึ้นอยู่กับกลุ่มมิติสินค้าคงคลังที่คุณแนบไว้กับสินค้านั้นๆ  วิธีนี้จะมีประโยชน์เมื่อคุณต้องการติดตามสินค้าที่วัตถุที่ให้บริการแสดงถึง 

    วัตถุที่ให้บริการที่มีตัวตนยังสามารถเป็นสินค้าที่ไม่เกี่ยวข้องโดยตรงกับการผลิตโดยตรงของบริษัท หรือห่วงโซ่การจัดหาวัสดุ  ตัวอย่างเช่น ชุดเครื่องมือที่ใช้สำหรับการซ่อมแซมใบสั่งบริการสามารถเป็นวัตถุที่ให้บริการที่ไม่ได้รวมอยู่ในสินค้าคงคลัง  ในกรณีนี้ คุณไม่ต้องลงทะเบียนไว้เป็นสินค้าคงคลัง

-  วัตถุที่ไม่สามารถจับต้องได้คือสิ่งที่เป็นนามธรรม เช่น ชุดบัญชีหรือเอกสารทางกฎหมายที่คุณสามารถทำงานบริการที่ดำเนินการ

## <a name="example-of-an-intangible-service-object"></a>ตัวอย่างของวัตถุที่ให้บริการที่ไม่มีตัวตน

บริษัท A รักษาเรกคอร์ดทางการเงินให้กับบริษัทขนาดเล็กจำนวนหนึ่ง  ลูกค้ารายหนึ่งของบริษัท A เป็นทีมฟุตบอลประจำท้องถิ่น ซึ่งบริษัทรับผิดชอบการทำบัญชีประจำสัปดาห์และตรวจสอบบัญชีประจำปีของสโมสร  บัญชีของสโมสรถูกตั้งค่าไว้ในแบบฟอร์มออบเจ็กต์ที่ให้บริการ และถูกกำหนดเป็นออบเจ็กต์ในข้อตกลงการให้บริการ  โดยมีรายการข้อตกลงการให้บริการสองรายการสำหรับวัตถุ  รายการ 1 เป็นการทำบัญชีประจำสัปดาห์ซึ่งมีระยะเวลาห่างหนึ่งครั้งต่อสัปดาห์ ในขณะที่รายการ 2 เป็นการตรวจสอบบัญชีประจำปีซึ่งมีระยะเวลาห่างหนึ่งครั้งต่อปี

## <a name="related-articles"></a>บทความที่เกี่ยวข้อง

[การสร้างวัตถุที่ให้บริการ](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]