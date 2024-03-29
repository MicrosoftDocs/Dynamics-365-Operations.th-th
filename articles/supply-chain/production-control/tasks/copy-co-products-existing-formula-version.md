---
title: คัดลอกสินค้าร่วมจากเวอร์ชั่นสูตรที่มีอยู่
description: 'กระบวนงานนี้แสดงวิธีการคัดลอกผลิตภัณฑ์ร่วมจากเวอร์ชันสูตรที่มีอยู่ ไปที่เวอร์ชันสูตรที่แตกต่างกันสำหรับผลิตภัณฑ์ที่นำออกใช้ '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 527fd94613d53a3f0ae81834d5bdaad30dca2833
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579243"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>คัดลอกสินค้าร่วมจากเวอร์ชั่นสูตรที่มีอยู่

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการคัดลอกผลิตภัณฑ์ร่วมจากเวอร์ชันสูตรที่มีอยู่ ไปที่เวอร์ชันสูตรที่แตกต่างกันสำหรับผลิตภัณฑ์ที่นำออกใช้  ซึ่งเป็นข้อกำหนดเบื้องต้นที่ต้องมีเวอร์ชันสูตรอย่างน้อยหนึ่งรายการที่เชื่อมโยงกับผลิตภัณฑ์ร่วม  เราจะใช้ข้อมูลสาธิตของบริษัท USP2 เพื่อสร้างขั้นตอนนี้


## <a name="find-a-released-product"></a>ค้นหาผลิตภัณฑ์ที่นำออกใช้
1. ไปที่ผลิตภัณฑ์ที่จะนำออกใช้
2. คลิกแสดงตัวกรอง
    * คุณกำลังจะเพิ่่มชนิดการผลิตฟิลด์ในกล่องข้อความตัวกรอง  
3. คลิกเพิ่มฟิลด์ตัวกรองเพื่อเพิ่มชนิดการผลิตฟิลด์
    * ในขั้นตอนต่อไป คุณต้องป้อนสูตรในฟิลด์ชนิดการผลิต ก่อนที่คุณจะเลือก นำไปใช้งาน  นี่จะตั้งค่าตัวกรองข้อมูลตามรายการของผลิตภัณฑ์ที่นำออกใช้  
4. ป้อนสูตรในฟิลด์ชนิดผลิตภัณฑ์ด้วยตนเอง
5. คลิก ใช้

## <a name="select-a-released-product"></a>ค้นหาผลิตภัณฑ์ที่นำออกใช้
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
2. คลิกเวอร์ชันสูตร
    * ในหน้าต่างการดำเนินการด้านวิศวกร คลิกเวอร์ชันของสูตร  

## <a name="copy-co-products"></a>คัดลอกผลิตภัณฑ์ร่วม
1. ในบานหน้าต่างการดำเนินการ คลิกเวอร์ชั่นสูตร
2. คลิกผลิตภัณฑ์ร่วม
3. คลิก คัดลอก
4. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
5. ในฟิลด์เวอร์ชันสูตร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
6. คลิก ตกลง
7. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]