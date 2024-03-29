---
title: สูตรและสูตรการผลิต
description: บทความนี้แสดงข้อมูลเกี่ยวกับสูตรการผลิต (BOM) และสูตร ซึ่งเป็นส่วนสำคัญของข้อกำหนดของผลิตภัณฑ์และผลิตภัณฑ์ย่อย
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace, ProdBOM, ProdJournalTransBOM, ProdBOMCurrent, PmfBOMDesignerEditCoBy, ProdJournalPickingListLineSummary, ProdBOMOverview, PmfCoReqPlanning, EcoResProductProdTypeFormulaNoActiveFormulaFormPart, EcoResItemsMissingActiveRouteVersionFormPart, EcoResItemsProdTypeBOMExpiringBOMFormPart, BOMDesignerBOMVersion, BOMExpandPurch, BOMChangeLine, BOMExpandSales, EcoResItemsProdTypeBOMExpiringRouteFormPart, EngChgEcmBomDesigner, EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmBOMCopyDialog, EngChgEcmBomDesignerEditBom, BOMDesignerFilterDialog, BOMDesignerFilterDialog, BOMPartOf, BOMSetupReportFinish, EcoResItemsMissingActiveBOMVersionFormPart, BOMIdLookup, EcoResProductProdTypeFormulaNoActiveRouteFormPart, BOMExpandPurchRFQ, EngChgCaseRouteTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57a30aba3b0a37d939d0747b2dd305a92c82ae23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887296"
---
# <a name="bills-of-materials-and-formulas"></a>สูตรและสูตรการผลิต

[!include [banner](../includes/banner.md)]

บทความนี้แสดงข้อมูลเกี่ยวกับสูตรการผลิต (BOM) และสูตร ซึ่งเป็นส่วนสำคัญของข้อกำหนดของผลิตภัณฑ์และผลิตภัณฑ์ย่อย BOM และสูตรระบุวัสดุหรือส่วนผสมที่จำเป็นสำหรับผลิตภัณฑ์เฉพาะ นอกจากนี้สูตรยังระบุสินค้าร่วมและสินค้าพลอยได้ที่ได้รับในบริบทการผลิตเฉพาะ 

## <a name="bills-of-materials"></a>สูตรการผลิต

สูตรการผลิต (BOM) กำหนดส่วนประกอบที่ต้องใช้เพื่อผลิตผลิตภัณฑ์ ส่วนประกอบอาจเป็นวัตถุดิบ ผลิตภัณฑ์กึ่งสำเร็จรูป หรือส่วนผสม ในบางกรณี การบริการสามารถถูกอ้างอิงใน BOM อย่างไรก็ตาม BOMs โดยทั่วไปหมายถึง *ทรัพยากรวัสดุ* ที่จำเป็นต้องมี  

เมื่อถูกผสมพร้อมกับกระบวนการผลิต หรือขั้นตอนการผลิตที่อธิบายการดำเนินงาน และทรัพยากรที่จำเป็นในการสร้างผลิตภัณฑ์ BOM เป็นข้อมูลพื้นฐานสำหรับการคำนวณต้นทุนที่ประเมินของผลิตภัณฑ์  

BOM เป็นเอนทิตีแต่ละรายการที่แสดงตามข้อมูลต่อไปนี้:

-   รหัส BOM
-   ชื่อ BOM
-   บรรทัด BOM ที่อธิบายส่วนประกอบและส่วนผสม
-   BOM เวอร์ชัน ซึ่งกำหนดผลิตภัณฑ์และรอบระยะเวลาที่ BOM สามารถใช้ได้

BOM หนึ่งอธิบายระดับเดียวที่ระบุ โดยรหัสเฉพาะ ส่วนประกอบอาจมี BOMs ของตนเองที่อ้างอิง โดยเวอร์ชัน BOM คุณสามารถแสดง และแก้ไขลำดับชั้นทั้งหมดของ BOMs สำหรับผลิตภัณฑ์เฉพาะในโปรแกรมออกแบบ BOM

### <a name="formulas-co-products-and-by-products"></a>สูตร,สินค้าร่วมและสินค้าพลอยได้

สูตรคือชนิดย่อยของ BOM ที่ใช้โดยทั่วไปสำหรับกระบวนการผลิต นอกเหนือจากส่วนประกอบและส่วนผสม สูตรอธิบายถึงผลิตภัณฑ์ร่วมและสินค้าพลอยได้ ในรุ่นจริง คำนิยามของผลิตภัณฑ์ร่วมและสินค้าพลอยได้ของสูตรจำเป็นต้องใช้รุ่นสูตร โดยทั่วไปจะมีกำหนดสูตรเฉพาะสำหรับผลิตภัณฑ์สำเร็จรูปหนึ่งๆ (สูตรหรือสินค้าที่วางแผน) ที่กำหนดไว้ในรุ่นสูตร

### <a name="boms-in-the-product-lifecycle"></a>BOMs ในวงจรผลิตภัณฑ์

ในวงจรผลิตภัณฑ์ อาจสร้าง BOM หลายชนิดสำหรับเหตุผลต่าง ๆ:

-   **ร่าง/ร่าง BOM** – BOM นี้ให้ประมาณการร่างของวัสดุที่จำเป็นในระยะเริ่มการออกแบบ และช่วยให้คุณประเมินต้นทุนคร่าวๆ และประเมินคุณลักษณะของผลิตภัณฑ์ โดยปกติ BOM นี้ไม่ได้ถูกใช้ในการวางแผนทรัพยากรขององค์กร (ERP)
-   **วิศวกรรม BOM** – BOM นี้โดยปกติจะใช้เมื่อคุณออกแบบผลิตภัณฑ์ที่ขึ้นอยู่กับกลุ่มผลิตภัณฑ์ที่มีอยู่ จัดโครงสร้าง Bom วิศวกรรมกระบวนการออกแบบ และจัดกลุ่มผลิตภัณฑ์ที่ซับซ้อนเป็นวิศวกรรมโมดูล สำหรับผลิตภัณฑ์อย่างง่าย คุณอาจจะวิศวกรรม BOMs สำหรับกระบวนการผลิตที่แท้จริง อย่างไรก็ตาม สำหรับผลิตภัณฑ์อื่น ๆ การวิศวกรรม BOM จะต้องถูกแปลงเป็นการผลิต BOM ที่แท้จริง การวิศวกรรม BOMS โดยทั่วไปจะแสดง โดยแฝงในลำดับชั้น BOM ถึงแม้ว่าการวิศวกรรม BOMs สามารถใช้สำหรับการวางแผนและการดำเนินการของการดำเนินงานผลิต วิธีการนี้อาจทำให้ไม่มีประสิทธิภาพ โดยเฉพาะอย่างยิ่งในการดำเนินงานที่ซ้ำกันที่ใบสั่งงานถูกสร้างหลายใบ
-   **การวางแผน BOM**– BOM นี้จะใช้เพื่อทำการวางแผนสำหรับความต้องการวัสดุ ความต้องการของส่วนประกอบและส่วนผสมถูกคำนวณตามความต้องการของผลิตภัณฑ์สำเร็จรูป เช่นเดียวกับการคิดต้นทุน BOMs การวางแผน BOMs อาจแสดงถึงการซื้อคละกันเฉพาะของวัสดุที่ใช้ในรอบระยะเวลา
-   **การผลิต BOM**– นี่คือ BOM แท้จริงที่ใช้สำหรับการผลิตเฉพาะหนึ่ง ๆ การผลิต BOM ต้องคำนึงถึงทรัพยากรจริงที่ใช้ในการผลิตเป็นผลิตภัณฑ์ เมื่อสร้างใบสั่งผลิต ใบสั่งชุดงาน หรือคัมบัง ระดับต่าง ๆ ของ BOMs ที่จะแสดง โดยแฝงจะยุบลงในระดับหนึ่ง และกระจายช่วงการดำเนินงานสำหรับใบสั่ง
-   **การคิดต้นทุน BOM** – BOM นี้ถูกใช้คำนวณต้นทุนที่ประเมินของผลิตภัณฑ์ ตัวอย่างเช่น คุณสามารถใช้การคิดต้นทุน BOM เมื่อใช้ต้นทุนมาตรฐาน หรือต้นทุนวางแผนที่ประเมินของผลิตภัณฑ์ที่กำหนดให้มีคำนวณ การคิดต้นทุน BOMs สามารถอ้างอิงถึงทรัพยากรเฉพาะที่คละกันและวัสดุที่คาดว่าจะใช้ ดังนั้น คุณสามารถใช้การคำนวณต้นทุน BOM เพื่อสร้างต้นทุนที่ประเมินตัวแทนสำหรับรอบระยะเวลา และช่วยคุณหลีกเลี่ยงผลต่างตามช่วงเวลา

ชนิดของ BOM ที่ใช้ในการดำเนินการจริง ขึ้นอยู่กับการใช้งาน และในสถานการณ์ทางธุรกิจและความต้องการ ในการใช้งานอย่างง่าย การวางแผน BOM, การผลิต BOM และการคำนวณต้นทุน BOM อาจเป็นแบบจำลองของ BOM หนึ่ง ในสภาพแวดล้อมที่มีการเปลี่ยนแปลงทางวิศวกรรมที่ใช้บ่อยและหลายกระบวนการสำรอง ชุดที่ชนิด BOM ที่ใหญ่กว่าอาจจะจำเป็นต้องใช้

### <a name="approval-of-boms-and-formulas"></a>การอนุมัติ BOMs และสูตร

BOM และสูตรแต่ละสูตรสามารถแยกอนุมัติ หรือไม่แยกอนุมัติก็ได้ โดยทั่วไป การอนุมัติ BOM หรือสูตรเกิดขึ้นเมื่อ BOM ที่เกี่ยวข้องรุ่นแรกได้รับอนุมัติ อย่างไรก็ตาม ในบางสถานการณ์ทางธุรกิจ การอนุมัติเหล่านี้อาจมีขั้นตอนต่าง ๆ แตกต่างกันในกระบวนการ และอาจเกี่ยวข้องกับเจ้าของกระบวนการอื่น  

โปรดสังเกตว่า ถ้า BOM ยังไม่ได้อนุมัติ รุ่น BOM ที่เกี่ยวข้องทั้งหมดจะยังไม่ได้อนุมัติ

## <a name="bom-and-formula-versions"></a>BOM และรุ่นสูตร
เพื่อเชื่อมโยงกับ BOM เฉพาะหรือสูตรเพื่อผลิตภัณฑ์ย่อยที่สามารถผลิตได้ คุณต้องสร้างรุ่น BOM หรือรุ่นสูตร การตรวจสอบรุ่นของ BOM และรุ่นสูตรสามารถเรียงตามรอบระยะเวลา ปริมาณ ไซต์ มิติของผลิตภัณฑ์เฉพาะ และเงื่อนไขอื่น ๆ รุ่นสูตรมีคุณลักษณะเพิ่มเติมสำคัญ เช่นผลตอบแทน ข้อกำหนดผลิตภัณฑ์ร่วมและสินค้าพลอยได้ และคำแนะนำการกระจายต้นทุนสำหรับสูตร

### <a name="approval-of-bom-and-formula-versions"></a>การอนุมัติ BOM และรุ่นสูตร

ก่อนที่รุ่นสูตรจะถูกใช้ในการวางแผนหรือกระบวนการผลิตต้องได้รับอนุมัติก่อน เมื่อรุ่น BOM ถูกอนุมัติ BOM ที่เกี่ยวข้องสามารถถูกอนุมัติได้ ขึ้นอยู่กับการเลือกของผู้ใช้และสิทธิของผู้ใช้ โปรดทราบว่า รุ่น BOM สามารถถูกอนุมัติเฉพาะเมื่อมี BOM ที่เกี่ยวข้องได้รับอนุมัติ

### <a name="activation-of-the-default-bom-or-formula-version"></a>การเรียกใช้ค่าเริ่มต้น BOM หรือเวอร์ชันสูตร

เพื่อที่จะตั้งค่าเฉพาะ BOM หรือสูตรเป็นค่าเริ่มต้นรุ่น BOM หรือรุ่นสูตรที่ถูกจะใช้โดยการวางแผนหลักหรือถูกใช้เพื่อสร้างใบสั่งผลิต คุณต้องเรียกใช้รุ่นดังกล่าว เมื่อรุ่นหนึ่งถูกเรียกใช้แล้ว การไม่ซ้ำกันของรุ่นสำหรับข้อจำกัดที่ระบุ (ตัวอย่างเช่น รอบระยะเวลา ไซต์ หรือปริมาณ) จะถูกตรวจสอบ คุณจะได้รับข้อผิดพลาดหากรุ่นที่คุณกำลังพยายามเรียกใช้ขัดแย้งกับรุ่นที่ทำงานอยู่แล้ว จากนั้นคุณต้องยกเลิกรุ่นที่ขัดแย้งหรือปรับเปลี่ยนข้อจำกัดของรุ่น (โดยปกติคือรอบระยะเวลา) เพื่อป้องกันการเรียกใช้ไม่ชัดเจน

### <a name="product-change-with-case-management"></a>การเปลี่ยนแปลงของผลิตภัณฑ์ด้วยการจัดการกรณี

กรณีการเปลี่ยนแปลงของผลิตภัณฑ์เพื่อการอนุมัติและเรียกใช้ใหม่หรือเปลี่ยนแปลง BOM และรุ่น BOM ทำให้มีวิธีที่ง่ายที่จะดูภาพรวมของข้อจำกัดของรุ่น BOM คุณสามารถอนุมัติ และเรียกใช้ BOM ทั้งหมดและสูตรที่เกี่ยวข้องกับการเปลี่ยนแปลงเฉพาะสำหรับวันเรียกใช้หนึ่งครั้ง

### <a name="alternative-bom-versions"></a>รุ่น BOM สำรอง

บางครั้ง รุ่น BOM ที่ใช้งานหรือรุ่นสูตรไม่ควรถูกใช้ในการคาดการณ์ การขาย หรือผลิตภัณฑ์หลัก ในกรณีนี้ คุณสามารถเลือก BOM ที่อนุมัติแล้วเฉพาะเป็นส่วนหนึ่งของความต้องการ (บรรทัดการคาดการณ์ บรรทัดการขาย หรือบรรทัด BOM) ถ้ารุ่น BOM ที่อนุมัติแล้วหรือรุ่นสูตรมีอยู่สำหรับการสำรอง BOM หรือสูตร  

เมื่อใบสั่งที่วางแผนไว้ ใบสั่งผลิต หรือคัมบังถูกสร้างขึ้น ผู้วางแผนหรือหัวหน้างานฝ่ายผลิตสามารถใช้เวอร์ชัน BOM ที่อนุมัติแล้วใด ๆ ที่มีผลบังคับใช้ในวันที่ร้องขอแผนการผลิตเพื่อที่จะวางแผนสำหรับการผลิตผลิตภัณฑ์เฉพาะหนึ่ง ๆ รุ่น BOM ที่ถูกใช้ไม่จำเป็นต้องถูกเรียกใช้เป็นรุ่นสูตร BOM เริ่มต้น

## <a name="bom-and-formula-lines"></a>รายการ BOM และ สูตร
รายการ BOM ถูกสร้างขึ้นสำหรับแต่ละวัสดุ บริการ หรือส่วนผสม รายการนั้นจะกำหนดปริมาณการใช้ที่วางแผนไว้ของผลิตภัณฑ์ย่อยที่ระบุ และยังกำหนดแอททริบิวต์ต่าง ๆ ที่เกี่ยวข้องกับปริมาณการใช้วัสดุที่วางแผนไว้  

รายการ BOM สามารถมีชนิดรายการต่อไปนี้: **สินค้า**, **Phantom**, **ซัพพลายที่ถูกเชื่อมโยง**, **ผู้จัดจำหน่าย**

### <a name="item"></a>สินค้า

เลือกชนิดรายการ **สินค้า** สำหรับวัสดุหรือบริการที่จะถูกใช้โดยตรง และไม่ต้องการกระจายไปไกลหรือการจัดหาวัสดุโยงรายการ

### <a name="phantom"></a>รายการแฝง

เลือกชนิดรายการ **Phantom** เมื่อคุณต้องการกระจายสินค้า BOM ระดับล่างใด ๆ ที่มีอยู่ในรายการ BOM ในการจัดกำหนดการหลัก ในการคำนวณต้นทุนที่วางแผนไว้ หรือในการประเมินของใบสั่งผลิตที่ใช้รายการ BOM ของชนิด **Phantom** รายการ BOM หลักที่อ้างอิงถึงผลิตภัณฑ์ย่อยที่ BOM Phantom ถูกแทนที่โดยสินค้าส่วนประกอบที่ถูกแสดงรายการเป็นรายการ BOM ใน BOM ดังที่กำหนดตามรุ่น BOM ที่ใช้งานอยู่ของผลิตภัณฑ์ย่อย ถ้าผลิตภัณฑ์ย่อยมีกระบวนการผลิตที่ใช้งานอยู่ การดำเนินงานของกระบวนการผลิตนั้นจะถูกรวมไว้ในกระบวนการหลัก  

โปรดทราบว่า Phantom โดยทั่วไปจะถูกใช้ในการทำให้กระบวนการทางวิศวกรรมง่ายขึ้น การใช้ Bom phantom ในหลายระดับได้มีผลต่อประสิทธิภาพการทำงาน โดยเฉพาะในสถานการณ์จำลองการผลิตซ้ำอย่างยิ่ง เพื่อที่จะปรับปรุงประสิทธิภาพ คุณควรหลีกเลี่ยงลำดับชั้นลึกของ Phantom เพื่อเป็นการแทน ใช้ BOM การผลิตแบบกระจายล่วงหน้าและกระบวนการผลิต

### <a name="pegged-supply"></a>การจัดหาวัสดุที่มีการเชื่อมโยงความต้องการกับการจัดซื้อ

เลือกชนิดรายการ **ซัพพลายที่ถูกเชื่อมโยง** เมื่อคุณต้องการสร้างการผลิตย่อย การคัมบังเหตุการณ์รายการ BOM หรือใบสั่งซื้อโดยตรงสำหรับผลิตภัณฑ์ย่อยใดๆที่อ้างอิงถึงรายการ BOM การผลิตย่อย เหตุการณ์ การคัมบัง หรือใบสั่งผลิตจะถูกสร้างขึ้นมาเมื่อคุณคาดคะเนใบสั่งผลิต ปริมาณสินค้าที่ต้องการจะถูกสำรองไว้โดยอัตโนมัติสำหรับใบสั่งการผลิตที่ใช้

### <a name="vendor"></a>ผู้จัดจำหน่าย

เลือกชนิดรายการ **ผู้จัดจำหน่าย** หากกระบวนการผลิตใช้ผู้รับเหมารายย่อย และคุณต้องการให้การผลิตย่อยหรือใบสั่งซื้อถูกสร้างขึ้นโดยอัตโนมัติสำหรับผู้รับเหมารายย่อย  

**หมายเหตุเกี่ยวกับการดำเนินการรับเหมารายย่อยใน BOM:** บริการหรืองานที่ดำเนินการ โดยผู้รับเหมาย่อยต้องถูกสร้างขึ้นเป็นสินค้าบริการที่ถูกติดตามในสินค้าคงคลัง คุณต้องแนบสินค้าบริการไปยังสินค้าหลักเป็นรายการ BOM กระบวนการผลิตต้องมีการดำเนินงานที่ถูกกำหนดให้กับทรัพยากรการดำเนินงานของผู้รับเหมารายย่อย





[!INCLUDE[footer-include](../../includes/footer-banner.md)]