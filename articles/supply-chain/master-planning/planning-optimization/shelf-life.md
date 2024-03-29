---
title: การวางแผนหลักของผลิตภัณฑ์ที่มีอายุการเก็บที่จํากัด
description: บทความนี้จะอธิบายวิธีการตั้งค่าและใช้คุณลักษณะการวางแผน โดยคิดจากอายุการเก็บผลิตภัณฑ์ที่สามารถผ่านได้
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 68a1ba2bfe90aaf0462917c405d483fa12bf8126
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428239"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>การวางแผนหลักของผลิตภัณฑ์ที่มีอายุการเก็บที่จํากัด

[!include [banner](../../includes/banner.md)]

อายุการเก็บสินค้าคือจํานวนเวลาที่สามารถใช้หรือขายผลิตภัณฑ์ได้ จนกว่าจะไม่สามารถใช้หรือขายผลิตภัณฑ์ได้อีกต่อไป เฉพาะผลิตภัณฑ์ที่มีอายุการเก็บสินค้าจํากัด คุณอาจใช้กลยุทธ์คลังสินค้าที่หมดอายุก่อน (FEFO) ออกใช้ก่อน (FEFO) ซึ่งจะจัดระดับของปริมาณการใช้และการขายสินค้าตามอายุการเก็บที่เหลือของผลิตภัณฑ์ กลยุทธ์คลังสินค้านี้เกี่ยวข้องกับอาหาร ยา และสินค้าอื่นๆ ที่จัดลักษณะตามเวลาการจัดเก็บสั้น ตาม FEFO สินค้าในคลังสินค้าจะถูกจัดเก็บไว้ เช่น สินค้าบนชั้นวางซุปเปอร์มาร์เก็ต ผลิตภัณฑ์ที่มีอายุการเก็บสินค้านานจะถูกวางลึกลงในชั้นวาง เพื่อให้ผลิตภัณฑ์ที่มีอายุการเก็บสินค้าที่สั้นกว่าถูกจัดส่งก่อน

## <a name="using-shelf-life-in-master-planning"></a>การใช้อายุการเก็บในการวางแผนหลัก

ส่วนนี้อธิบายวิธีที่การวางแผนหลักแนะนาในการจัดหาวัสดุของสินค้าที่มีอายุการเก็บสินค้า

เมื่อคุณรันแผนหลัก แผนหลักจะสร้างแผนการใบสั่ง (การจัดหาวัสดุ) ที่แนะนำ ซึ่งจะตอบสนองความต้องการของคุณ และลดความล่าช้าให้เหลือมากที่สุด ถ้าแผนของคุณรวมสินค้าที่มีอายุการเก็บสินค้าที่จํากัด การคํานวณการวางแผนจะซับซ้อนมากขึ้น เนื่องจากแผนต้องไม่เพียงลดความล่าช้าลงเท่านั้น แต่ยังใช้การจัดหาวัสดุที่มีอยู่ก่อนที่จะหมดอายุ แผนต้องพยายามใช้อุปทานที่ใกล้กับวันหมดอายุที่ใกล้ที่สุด ก่อนที่จะมีการจัดหาวัสดุที่หมดอายุในภายหลัง ดังนั้น การวางแผนหลักจึงต้องบรรลุเป้าหมายต่อไปนี้ ตามลำดับ

1. ลดผลรวมของความล่าช้า
1. เพิ่มผลรวมของการจัดหาวัสดุ FEFO
1. ลดการเพิ่มเติมสินค้าของสินค้าคงคลัง

ในบางกรณี อาจมีความขัดแย้งระหว่างสองเป้าหมายแรกและต้องมีตัวเลือก: คุณต้องการหน่วงเวลาการจัดส่ง หรือคุณต้องการใช้อุปทานที่หมดอายุในภายหลังแทนอุปทานที่จะหมดอายุในไม่ช้าหรือไม่ เมื่อต้องการแก้ไขความขัดแย้งนี้ในระหว่างการวางแผนหลัก ระบบจะจัดระดับการลดความล่าช้า เมื่อใช้การจัดหาวัสดุที่ใกล้หมดอายุขึ้น โดยทั่วไปแล้ว ชนิดของความขัดแย้งนี้จะเกิดขึ้นเมื่ออาจมีความล่าช้าและครอบคลุมตามรอบระยะเวลา ดังนั้น ขอแนะนำว่าคุณควรใช้รอบระยะเวลาความครอบคลุมที่สั้นกว่าอายุการเก็บสินค้าหนึ่งๆ ความครอบคลุมชนิดอื่นๆ (เช่น ความต้องการ) เป็นไปได้ว่าอาจไม่พบความขัดแย้งชนิดนี้

## <a name="set-up-shelf-life"></a>ตั้งค่าอายุการเก็บสินค้า

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>ตั้งค่าคอนฟิกแผนหลักแต่ละแผน ให้พิจารณาอายุการเก็บสินค้า

ตามค่าเริ่มต้น แผนหลักจะไม่พิจารณาอายุการเก็บสินค้า ใช้ขั้นตอนต่อไปนี้เพื่อเปิดใช้งานการคํานวณอายุการเก็บสินค้าของแผนหลักแต่ละแผนที่ต้องการใช้

1. ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก**
1. เลือกแผนหลักในบานหน้าต่างรายการ หรือสร้างแผนหลักใหม่
1. บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **ใช้วันที่อายุการเก็บ** เป็น *ใช่*

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>ตั้งค่าคอนฟิกกลุ่มมิติการติดตาม เพื่อติดตามมิติชุดงาน

สามารถติดตามอายุการเก็บสินค้าของสินค้าได้เฉพาะเมื่อสินค้านั้นถูกติดตามที่มิติชุดงานเท่านั้น หรือกล่าวอีกอย่างคือ ต้องมีการบันทึกข้อมูลอ้างอิงชุดงานและวันที่ที่ต้องการเมื่อมีการรับสินค้าหรือการผลิต และต้องผ่านรายการความเคลื่อนไหวของสินค้าคงคลังทุกรายการของสินค้านั้น เมื่อต้องการจัดการตัวเลือกนี้ ให้ตั้งค่ากลุ่มมิติการติดตามหนึ่งกลุ่มขึ้นไปเพื่อติดตามที่ต้องการ และกําหนดสินค้าที่เกี่ยวข้องให้กับกลุ่มเหล่านี้ตามที่ต้องการ

ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่ากลุ่มมิติการติดตามเพื่อติดตามมิติชุดงาน

1. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> มิติและกลุ่มตัวแปร \> กลุ่มมิติการติดตาม**
1. ทำตามขั้นตอนเหล่านี้

    - ในบานหน้าต่างการดำเนินการ เลือก **ใหม่** เพื่อสร้างกลุ่มมิติการติดตามใหม่ ป้อนชื่อและคำอธิบาย จากนั้นเลือก **บันทึก** บนบานหน้าต่างการดำเนินการ
    - ในบานหน้าต่างรายการ ให้เลือกกลุ่มมิติการติดตามที่มีอยู่ซึ่งคุณต้องการตั้งค่าเพื่อติดตามมิติชุดงาน

1. บนแท็บด่วน **มิติการติดตาม** ในแถว **หมายเลขชุดงาน** ให้เลือกกล่องกาเครื่องหมายในคอลัมน์ **ที่ใช้งานอยู่** และ **สินค้าคงคลังที่มีอยู่จริง**

### <a name="set-up-shelf-life-for-a-product"></a>ตั้งค่าอายุการเก็บสินค้าของผลิตภัณฑ์

ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าอายุการเก็บผลิตภัณฑ์

1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**
1. สร้างหรือเปิดผลิตภัณฑ์ที่คุณต้องการตั้งค่า
1. หากต้องการใช้การตั้งค่าอายุการเก็บสินค้า บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าฟิลด์ **กลุ่มมิติการติดตาม** เป็นกลุ่มมิติการติดตาม ที่มีการตั้งค่าให้ติดตามมิติชุดงาน คุณสามารถตั้งค่าฟิลด์นี้ได้เฉพาะเมื่อคุณสร้างผลิตภัณฑ์ครั้งแรกเท่านั้น คุณไม่สามารถเปลี่ยนค่าจากผลิตภัณฑ์ที่มีอยู่
1. บนแท็บด่วน **จัดการสินค้าคงคลัง** ตั้งค่าฟิลด์ต่อไปนี้:

    - **รอบระยะเวลาของคำแนะนำการเก็บสินค้าที่มีหน่วยเป็นวัน** – ระบุรอบระยะเวลา (เป็นวัน) ซึ่งจะตรวจสอบชุดงานของผลิตภัณฑ์นี้ เพื่อให้แน่ใจว่าสินค้าที่เหมาะสมกับปริมาณการใช้หรือนําไปขายต่อ ค่าของฟิลด์นี้จะถูกเพิ่มเข้าใน *วันที่ผลิต* ของชุดงาน เพื่อระบุ *วันที่แนะนำการเก็บสินค้า* ของชุดงาน คุณสามารถตั้งค่าคอนฟิกระบบเพื่อสร้างใบสั่งตรวจสอบคุณภาพ เมื่อชุดงานเข้าใกล้วันที่แนะนําการเก็บสินค้า
    - **รอบระยะเวลาสำหรับอายุการเก็บสินค้าเป็นวัน** – ระบุจํานวนวันก่อนที่ชุดงานของผลิตภัณฑ์นี้จะหมดอายุ ค่านี้จะถูกเพิ่มใน *วันที่ผลิต* เพื่อระบุ *วันหมดอายุ* ชุดงานถือว่าใช้ไม่ได้หลังจากวันที่นี้
    - **รอบระยะเวลาที่ควรใช้ก่อนที่มีหน่วยเป็นวัน** – ระบุรอบระยะเวลา (เป็นวัน) ซึ่งชุดงานของผลิตภัณฑ์นี้ยังคงขายได้ แต่ไม่สามารถรักษาคุณสมบัติเดิมบางอย่างของชุดงานได้อีกต่อไป ค่านี้จะถูกเพิ่มใน *วันที่ผลิต* เพื่อระบุ *วันที่ควรใช้ก่อน* คุณสามารถรันรายงานเพื่อระบุสินค้าคงคลังที่เลยวันที่ควรใช้ก่อน 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>ตั้งค่ากฎวันที่ขายได้ของลูกค้าแต่ละคน

ฟังก์ชัน *วันที่ขายได้* ช่วยให้มั่นใจว่าผลิตภัณฑ์จากชุดงานที่ใกล้หมดอายุจะไม่ถูกส่งให้กับลูกค้า นอกจากนี้ ยังช่วยให้มั่นใจว่าเมื่อส่งผลิตภัณฑ์ให้กับลูกค้า จํานวนวันที่ขายได้เพียงพอจะยังคงเหลืออยู่หลังจากการจัดส่ง

หากต้องการใช้ฟังก์ชันวันที่ขายได้ คุณต้องกําหนดจํานวนวันที่ขายได้ที่ใช้กับผลิตภัณฑ์แต่ละรายการ (หรือกลุ่มผลิตภัณฑ์) ของลูกค้าแต่ละคน คุณต้องดำเนิการกระบวนการนี้ให้เสร็จสมบูรณ์ด้วยตนเอง เนื่องจากไม่มีเอนทิตี้ข้อมูล

ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าวันที่ขายได้ของผลิตภัณฑ์แต่ละรายการของลูกค้าแต่ละคน

1. ไปที่ **การขายและการตลาด \> ลูกค้า \> ลูกค้าทั้งหมด**
1. ค้นหาและเลือกลูกค้าที่คุณต้องการตั้งค่า
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **การขาย** ในกลุ่ม **การตั้งค่า** ให้เลือก **การขาย \> วันที่ขายได้**
1. ในหน้า **วันที่ขายได้ของลูกค้า** กริดจะแสดงรายการกฎวันที่ขายได้ที่มีอยู่ให้กับแต่ละผลิตภัณฑ์หรือกลุ่มผลิตภัณฑ์ ใช้ปุ่มบนบานหน้าต่างการดำเนินการ เพื่อเพิ่มหรือแก้ไขแถวในกริด ตามต้องการ มี **ตัวกรอง** เพื่อช่วยคุณค้นหาแถวที่มีอยู่
1. สำหรับแต่ละแถว กำหนดค่าฟิลด์ต่อไปนี้:

    - **รหัสสินค้า** – ให้เลือกหนึ่งในค่าต่อไปนี้ เพื่อระบุขอบเขตของสินค้าที่จะได้รับผลกระทบ:

        - *ตาราง* – แถวจะใช้กับสินค้าเฉพาะ
        - *กลุ่ม* – แถวจะใช้กับกลุ่มสินค้าเฉพาะ
        - *ทั้งหมด* – แถวจะใช้กับสินค้าทั้งหมด

    - **ความสัมพันธ์ของสินค้า** – ถ้าคุณตั้งค่าฟิลด์ **รหัสสินค้า** เป็น *ตาราง* ให้เลือกสินค้าเฉพาะ ถ้าคุณตั้งค่าฟิลด์ **รหัสสินค้า** เป็น *กลุ่ม* ให้เลือกกลุ่มสินค้า ถ้าคุณตั้งค่าฟิลด์ **รหัสสินค้า** เป็น *ทั้งหมด* ฟิลด์นี้จะไม่พร้อมใช้งาน
    - **วันที่ขายได้** – ป้อนจํานวนวันต่ำสุดที่ลูกค้าต้องขายผลิตภัณฑ์ที่ตรงกัน ก่อนที่ชุดงานจะหมดอายุ ค่าวันที่ขายได้จะขึ้นอยู่กับวันที่รับสินค้าที่ร้องขอ (หรือวันที่ยืนยันการรับสินค้า ถ้ากําหนดไว้) ให้กับผลิตภัณฑ์ที่ตรงกันในใบสั่งขาย
    - *(มิติของผลิตภัณฑ์อื่นๆ)* – เพื่อจํากัดขอบเขตของแถวเพิ่มเติม ให้ระบุค่ามิติอื่นๆ (เช่น **ขนาด** และ **สี**) ตามที่ต้องการ ในการควบคุมมิติที่แสดงในกริด ให้เลือก **มิติการแสดงผล** บนบานหน้าต่างการดำเนินการ

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>ตั้งค่าผลิตภัณฑ์ที่เกี่ยวข้องทั้งหมด เพื่อให้มีการควบคุมวันที่ FEFO

เพื่อให้วันที่ขายได้ทำงาน สินค้าที่เกี่ยวข้องแต่ละรายการต้องอยู่ในกลุ่มแบบจำลองสินค้าที่มีการเลือกกล่องกาเครื่องหมาย **FEFO ที่ควบคุมด้วยวันที่**

ใช้กระบวนงานต่อไปนี้ เพื่อตั้งค่ากลุ่มแบบจำลองสินค้าเพื่อให้ระบบสนับสนุนฟังก์ชันวันที่ขายได้

1. ไปที่ **การจัดการสินค้าคงคลัง \> การตั้งค่า \> สินค้าคงคลัง \> กลุ่มแบบจำลองสินค้า**
1. เลือกกลุ่มที่มีอยู่ในบานหน้าต่างรายการ หรือสร้างนโยบายใหม่โดยการเลือก **สร้าง** ในบานหน้าต่างการดำเนินการ
1. บนแท็บด่วน **นโยบายสินค้าคงคลัง** ให้เลือกกล่องกาเครื่องหมาย **FEFO ที่ควบคุมด้วยวันที่**
1. ตั้งค่าฟิลด์สำหรับกลุ่มอื่นตามที่คุณต้องการ

ใช้กระบวนงานต่อไปนี้ เพื่อดูหรือตั้งค่ากลุ่มแบบจำลองสินค้าที่ผลิตภัณฑ์เป็นสมาชิกอยู่

1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**
1. เปิดผลิตภัณฑ์ที่คุณต้องการตรวจสอบหรือแก้ไข
1. บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าฟิลด์ **กลุ่มแบบจำลองสินค้า** เป็นกลุ่มที่มีการเลือกกล่องกาเครื่องหมาย **FEFO ที่ควบคุมด้วยวันที่** ไว้

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>ตัวอย่างที่ 1: Simple FEFO, รอบระยะเวลา 10 วัน, ศูนย์วันของระยะเวลารอคอยสินค้า

ตัวอย่างนี้แสดงตัวอย่างพื้นฐานของอายุการเก็บสินค้า ที่ทำตามการเชื่อมโยงความต้องการกับการจัดซื้อระหว่างใบสั่งจัดหาวัสดุและความต้องการ เพื่อให้เป็นไปตามเป้าหมายต่อไปนี้ของระบบ:

- ลดผลรวมของความล่าช้า
- เพิ่มผลรวมของการจัดหาวัสดุ FEFO
- ลดการเพิ่มเติมสินค้าของสินค้าคงคลัง

ระบบมีการตั้งค่าสินค้าและแผนหลักต่อไปนี้:

- **รหัสความครอบคลุม (กลยุทธ์การเติมสินค้า):** รอบระยะเวลา 
- **รอบระยะเวลาความครอบคลุม:** 10 วัน (เท่ากับอายุการเก็บสินค้า)
- **อายุการเก็บ:** 10 วัน
- **วันที่ขายได้:** 0 วัน
- **ระยะเวลารอคอยสินค้า:** 0 วัน
- **จำนวนวันค่าลบ:** 0 วัน
- **ชนิดของแผนการใบสั่ง (การตั้งค่าใบสั่งเริ่มต้นของสินค้า):** ใบสั่งซื้อ

ใบสั่งขายต่อไปนี้มีสินค้าอยู่ในระบบ:

- **SO1:** ปริมาณ (ปริมาณ) = 2, วันที่จัดส่งที่ร้องขอ = วันนี้ + 1 วัน
- **SO2:** ปริมาณ = 1, วันที่จัดส่งที่ร้องขอ = วันนี้ + 4 วัน
- **SO3:** ปริมาณ = 1, วันที่จัดส่งที่ร้องขอ = วันนี้ + 5 วัน

ใบสั่งขายเหล่านี้ทั้งหมดสร้างความต้องการสินค้า

การจัดหาวัสดุต่อไปนี้สำหรับสินค้า:

- **ปริมาณสินค้าคงคลังคงเหลือ:** ปริมาณ = 1, วันหมดอายุ = วันนี้ + 5 วัน
- **ใบสั่งซื้อ 1 (PO1):** วันที่รับสินค้า = วันนี้ + 2 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 4 วัน

ระบบจะสร้างรายการการจัดหาวัสดุที่สามารถครอบคลุมความต้องการนี้ และเรียงลำกับรายการตามวันหมดอายุ (โดยใช้ FEFO)

การวางแผนหลักสร้างการเชื่อมโยงความต้องการกับการจัดซื้อระหว่างการจัดหาวัสดุและความต้องการ และยังสร้างความต้องการที่ต้องใช้ตามรายการจัดหาวัสดุ (โดยใช้ FEFO) และพิจารณาวันที่ที่พร้อมใช้งาน

- SO1 สามารถเติมสินค้าโดยใช้ปริมาณคงคลังคงเหลือได้ แต่ PO1 ไม่สามารถเติมสินค้าได้ เนื่องจากวันที่พร้อมใช้งานของ PO1 เป็นหนึ่งวันที่หลังจาก SO1 ต้องการ ดังนั้น SO1 จึงสร้างความต้องการสินค้าหนึ่งหน่วย
- PO1 สามารถครอบคลุม SO2 ได้ เนื่องจาก PO1 จะมาถึงภายในเวลาที่ร้องขอ และวันหมดอายุจะยังคงมีผลบังคับใช้ ดังนั้น PO1 จึงครอบคลุมความต้องการ SO2 ทั้งหมด
- SO3 ไม่ครอบคลุม เนื่องจากทรัพยากรไม่พร้อมใช้งาน ดังนั้น SO3 จึงสร้างความต้องการสินค้าหนึ่งหน่วย

เพื่อครอบคลุมความต้องการที่เหลือทั้งหมด ระบบต้องสร้างแผนการใบสั่งซื้อต่อไปนี้:

- **PPO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 2, วันหมดอายุ = วันนี้ + 10 วัน

ตารางต่อไปนี้สรุปผลลัพธ์

| ความต้องการ | การเชื่อมโยงความต้องการกับการจัดซื้อ |
|---|---|
| **SO1:** วันที่จัดส่ง = วันนี้ + 1 วัน, ปริมาณ = 2 | <p>**ปริมาณคงคลังคงเหลือ:** ปริมาณ = 1, วันหมดอายุ = วันนี้ + 5 วัน</p><p>**PPO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน</p> |
| **SO2:** วันที่จัดส่ง = วันนี้ + 4 วัน, ปริมาณ = 1 | **PO1:** วันที่รับสินค้า = วันนี้ + 2 วัน, 1 ปริมาณ, วันหมดอายุ = วันนี้ + 4 วัน |
| **SO3:** วันที่จัดส่ง = วันนี้ + 5 วัน, ปริมาณ = 1 | **PPO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 2, วันหมดอายุ = วันนี้ + 10 วัน |

ภาพประกอบต่อไปนี้แสดงเส้นเวลาสำหรับตัวอย่างนี้

![ตัวอย่างที่ 1: Simple FEFO, รอบระยะเวลา 10 วัน, ศูนย์วันของระยะเวลารอคอยสินค้า](media/fefo-example-1.png "ตัวอย่างที่ 1: Simple FEFO, รอบระยะเวลา 10 วัน, ศูนย์วันของระยะเวลารอคอยสินค้า")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>ตัวอย่างที่ 2: Simple FEFO, ความต้องการ, สามวันของระยะเวลารอคอยสินค้า

ตัวอย่างนี้แสดงวิธีการที่ความพยายามของระบบเพื่อลดความล่าช้า ในบางครั้งอาจทําให้การสั่งซื้อเกินเกิดขึ้น

ระบบมีการตั้งค่าสินค้าและแผนหลักต่อไปนี้:

- **รหัสความครอบคลุม (กลยุทธ์การเติมสินค้า):** ความต้องการ
- **อายุการเก็บ:** 10 วัน
- **วันที่ขายได้:** 0 วัน
- **ระยะเวลารอคอยสินค้า:** สร้างตามข้อตกลงทางการค้าของผู้ขายต่อไปนี้:

    - **ข้อตกลงทางการค้า1:** ถ้าปริมาณ = 1, ระยะเวลารอคอยสินค้า = 4
    - **ข้อตกลงทางการค้า 2:** ถ้าปริมาณ = 2, ระยะเวลารอคอยสินค้า = 3

- **จำนวนวันค่าลบ:** 0 วัน
- **ชนิดของแผนการใบสั่ง (การตั้งค่าใบสั่งเริ่มต้นของสินค้า):** ใบสั่งซื้อ

ใบสั่งขายต่อไปนี้มีอยู่ในระบบ

- **SO1:** ปริมาณ = 2, วันที่จัดส่งที่ร้องขอ = วันนี้ + 3 วัน

ความต้องการนี้ครอบคลุมโดยการจัดหาวัสดุที่มีอยู่และใบสั่งซื้อที่ยืนยันแล้ว:

- **ปริมาณสินค้าคงคลังคงเหลือ:** พร้อมใช้งาน = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 2 วัน
- **PO1:** วันที่รับสินค้า = วันนี้ + 3 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 4 วัน

SO1 ไม่สามารถตอบสนองด้วยปริมาณคงคลังคงเหลือได้ เนื่องจากวันหมดอายุของสินค้าคงคลังอยู่ก่อนวันที่จัดส่ง PO1 สามารถครอบคลุมความต้องการ SO1 ที่มีปริมาณเป็น 1 เท่านั้น ดังนั้น SO1 จึงสร้างความต้องการสินค้าหนึ่งหน่วย เพื่อครอบคลุมความต้องการนี้ ระบบจะสร้างแผนการใบสั่งซื้อ (PPO1)

ระบบมีข้อตกลงทางการค้าสองฉบับ (ข้อตกลงหนึ่งสำหรับปริมาณ = 1, ระยะเวลารอคอยสินค้า = 4 วัน และอีกข้อตกลงหนึ่งสำหรับปริมาณ = 2, ระยะเวลารอคอยสินค้า = 3 วัน) ดังนั้น ระบบจะพยายามลดความล่าช้าให้ต่ำสุด โดยการสร้างแผนการใบสั่งซื้อ (PPO1) ที่ตรงตามข้อตกลงทางการค้าที่สอง ผลลัพธ์คือการจัดส่งมากกว่าปริมาณที่จ่าย (ปริมาณ = 2 วันหมดอายุ = วันนี้ + 10 วัน)

ตารางต่อไปนี้สรุปผลลัพธ์

| ความต้องการ | การเชื่อมโยงความต้องการกับการจัดซื้อ |
|---|---|
| **SO1:** วันที่จัดส่ง = วันนี้ + 3 วัน, ปริมาณ = 2 | <p>**PO1:** วันที่รับสินค้า = วันนี้ + 3 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 4 วัน</p><p>**PPO1:** วันที่รับสินค้า = วันนี้ + 3 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน</p> |

ภาพประกอบต่อไปนี้แสดงเส้นเวลาสำหรับตัวอย่างนี้

![ตัวอย่างที่ 2: Simple FEFO, ความต้องการ, สามวันของระยะเวลารอคอยสินค้า](media/fefo-example-2.png "ตัวอย่างที่ 2: Simple FEFO, ความต้องการ, สามวันของระยะเวลารอคอยสินค้า")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>ตัวอย่างที่ 3: Simple FEFO, ความต้องการ, สามวันของระยะเวลารอคอยสินค้า, วันที่ขายได้ห้าวัน

ตัวอย่างนี้แสดงวิธีการทำงานของอายุการเก็บสินค้า เมื่อเพิ่มวันที่ขายได้ของสินค้า

ระบบมีการตั้งค่าสินค้าและแผนหลักต่อไปนี้:

- **รหัสความครอบคลุม (กลยุทธ์การเติมสินค้า):** ความต้องการ
- **อายุการเก็บ:** 10 วัน
- **วันที่ขายได้:** 5 วัน
- **ระยะเวลารอคอยสินค้า:** 5 วัน
- **จำนวนวันค่าลบ:** 0 วัน
- **ชนิดของแผนการใบสั่ง (การตั้งค่าใบสั่งเริ่มต้นของสินค้า):** ใบสั่งซื้อ

ใบสั่งขายต่อไปนี้มีอยู่ในระบบ:

- **SO1:** ปริมาณ = 2, วันที่จัดส่งที่ร้องขอ = วันนี้ + 2 วัน
- **SO2:** ปริมาณ = 1, วันที่จัดส่งที่ร้องขอ = วันนี้ + 3 วัน
- **SO3:** ปริมาณ = 1, วันที่จัดส่งที่ร้องขอ = วันนี้ + 5 วัน

ความต้องการนี้ครอบคลุมได้โดยการจัดหาวัสดุที่มีอยู่และใบสั่งซื้อที่ยืนยันแล้ว:

- **ปริมาณสินค้าคงคลังคงเหลือ:** พร้อมใช้งาน = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 6 วัน
- **PO1:** วันที่รับสินค้า = วันนี้ + 2 วัน, ปริมาณ = 3, วันหมดอายุ = วันนี้ + 10 วัน

ระบบจะสร้างรายการตัวเลือกการเชื่อมโยงความต้องการกับการจัดซื้อ ที่ขึ้นอยู่กับรายการการจัดหาวัสดุ (FEFO) และวันที่ที่พร้อมใช้ ดังนั้น SO1 จึงไม่สามารถตอบสนองโดยปริมาณคงคลังคงเหลือได้ เนื่องจากสินค้าคงคลังจะหมดอายุก่อนสิ้นสุดวันที่ขายได้ซึ่งลูกค้าต้องการ (วันที่ขอรับสินค้า + 5 วัน) PO1 สามารถครอบคลุมความต้องการ SO1 ที่มีสองหน่วย และความต้องการ SO2 ที่มีหนึ่งหน่วย ดังนั้น SO3 เท่านั้นที่ยังคงไม่ครอบคลุมความต้องการของสินค้าหนึ่งหน่วย เพื่อครอบคลุมความต้องการนี้ ระบบจะสร้างแผนการใบสั่งซื้อต่อไปนี้:

- **PP01:** วันที่รับสินค้า = วันนี้ + 5 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน

ตารางต่อไปนี้สรุปผลลัพธ์

| ความต้องการ | การเชื่อมโยงความต้องการกับการจัดซื้อ |
|---|---|
| **SO1:** วันที่จัดส่ง = วันนี้ + 2 วัน, ปริมาณ = 2 | **PO1:** วันที่รับสินค้า = วันนี้ + 2 วัน, ปริมาณ = 2, วันหมดอายุ = วันนี้ + 10 วัน |
| **SO2:** วันที่จัดส่ง = วันนี้ + 3 วัน, ปริมาณ = 1 | **PO1:** วันที่รับสินค้า = วันนี้ + 2 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน |
| **SO3:** วันที่จัดส่ง = วันนี้ + 5 วัน, ปริมาณ = 1 | **PPO1:** วันที่รับสินค้า = วันนี้ + 5 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน |

ภาพประกอบต่อไปนี้แสดงเส้นเวลาสำหรับตัวอย่างนี้

![ตัวอย่างที่ 3: Simple FEFO, ความต้องการ, สามวันของระยะเวลารอคอยสินค้า, วันที่ขายได้ห้าวัน](media/fefo-example-3.png "ตัวอย่างที่ 3: Simple FEFO, ความต้องการ, สามวันของระยะเวลารอคอยสินค้า, วันที่ขายได้ห้าวัน")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>ตัวอย่างที่ 4: Simple FEFO รอบระยะเวลา, ระยะเวลารอคอยสินค้าขึ้นอยู่กับปริมาณ

ตัวอย่างนี้แสดงวิธีการที่ความพยายามของระบบเพื่อลดความล่าช้า ในบางครั้งอาจทําให้การสั่งซื้อเกินเกิดขึ้น

ระบบมีการตั้งค่าสินค้าและแผนหลักต่อไปนี้:

- **รหัสความครอบคลุม (กลยุทธ์การเติมสินค้า):** รอบระยะเวลา
- **รอบระยะเวลาความครอบคลุม:** 10 วัน (เท่ากับอายุการเก็บสินค้า)
- **อายุการเก็บ:** 10 วัน
- **วันที่ขายได้:** 0 วัน
- **ระยะเวลารอคอยสินค้า:** สร้างตามข้อตกลงทางการค้าของผู้ขายต่อไปนี้:

    - **ข้อตกลงทางการค้า 1:** ถ้าปริมาณ = 1, ระยะเวลารอคอยสินค้า = 5
    - **ข้อตกลงทางการค้า 2:** ถ้าปริมาณ = 2, ระยะเวลารอคอยสินค้า = 0

- **จำนวนวันค่าลบ:** 0 วัน
- **ชนิดของแผนการใบสั่ง (การตั้งค่าใบสั่งเริ่มต้นของสินค้า):** ใบสั่งซื้อ

ใบสั่งขายต่อไปนี้มีอยู่ในระบบ:

- **SO1:** ปริมาณ = 1, วันที่จัดส่งที่ร้องขอ = วันนี้
- **SO2:** ปริมาณ = 1, วันที่จัดส่งที่ร้องขอ = วันนี้ + 6 วัน

ความต้องการนี้สามารถครอบคลุมบางส่วนโดยการจัดหาวัสดุที่มีอยู่จากใบสั่งซื้อที่ยืนยันแล้วต่อไปนี้:

- **PO1:** วันที่รับสินค้า = วันนี้ + 1 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 2 วัน
- **PO2:** วันที่รับสินค้า = วันนี้ + 3 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 7 วัน

ระบบมีข้อตกลงทางการค้าสองฉบับ (ข้อตกลงหนึ่งสำหรับปริมาณ = 1, ระยะเวลารอคอยสินค้า = 5 วัน และอีกข้อตกลงหนึ่งสำหรับปริมาณ = 2, ระยะเวลารอคอยสินค้า = 0 วัน) ดังนั้น ระบบจะพยายามลดความล่าช้าให้ต่ำสุด โดยการสร้างแผนการใบสั่งซื้อต่อไปนี้ ที่ตรงตามข้อตกลงทางการค้าที่สอง:

- **PP01:** วันที่รับสินค้า = วันนี้, ปริมาณ = 2, วันหมดอายุ = วันนี้ + 10 วัน

SO1 จะถูกครอบคลุมโดยหน่วยงานหนึ่งจาก PPO1 PO2 จะถูกครอบคลุมโดย PO2 เนื่องจาก PO2 หมดอายุเร็วกว่า PPO1

ตารางต่อไปนี้สรุปผลลัพธ์

| ความต้องการ | การเชื่อมโยงความต้องการกับการจัดซื้อ |
|---|---|
| **SO1:** วันที่จัดส่ง = วันนี้, ปริมาณ = 1 | **PPO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน |
| **SO2:** วันที่จัดส่ง = วันนี้ + 6 วัน, ปริมาณ = 1 | **PO2:** วันที่รับสินค้า = วันนี้ + 3 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 7 วัน |

> [!NOTE]
> PO1 ไม่ได้ใช้ เนื่องจากจะมาถึงช้าเกินไปสำหรับ S01 และจะหมดอายุก่อนที่ S02 จะถูกจัดส่ง PPO1 มีการจัดสินค้ามากเกินหนึ่งหน่วย เพื่อให้ระยะเวลารอคอยสินค้าเป็น 0 (ศูนย์) ต่อข้อตกลงทางการค้า 2

ภาพประกอบต่อไปนี้แสดงเส้นเวลาสำหรับตัวอย่างนี้

![ตัวอย่างที่ 4: Simple FEFO รอบระยะเวลา, ระยะเวลารอคอยสินค้าขึ้นอยู่กับปริมาณ](media/fefo-example-4.png "ตัวอย่างที่ 4: Simple FEFO รอบระยะเวลา, ระยะเวลารอคอยสินค้าขึ้นอยู่กับปริมาณ")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>ตัวอย่างที่ 5: Simple FEFO ความต้องการ, 10 วันที่ติดลบ

ตัวอย่างนี้แสดงวิธีการทำงานของอายุการเก็บสินค้า เมื่อจำนวนวันที่ติดลบหลายวันถูกเพิ่มให้กับสินค้า วันที่ติดลบแสดงถึงจำนวนของวันที่คุณเต็มใจรอ ก่อนที่คุณจะสั่งการเติมสินค้าสำหรับสินค้าที่มีสินค้าคงคลังค่าลบ ระบบไม่ได้สร้างอุปทาน เว้นแต่จะเกินจํานวนวันที่ติดลบ

ระบบมีการตั้งค่าสินค้าและแผนหลักต่อไปนี้:

- **รหัสความครอบคลุม (กลยุทธ์การเติมสินค้า):** ความต้องการ
- **ระยะเวลารอคอยสินค้า:** 0 วัน
- **จำนวนวันค่าลบ:** 10 วัน
- **ชนิดของแผนการใบสั่ง (การตั้งค่าใบสั่งเริ่มต้นของสินค้า):** ใบสั่งซื้อ

ใบสั่งขายต่อไปนี้มีอยู่ในระบบ

- **SO1:** ปริมาณ = 1, วันที่จัดส่งที่ร้องขอ = วันนี้

ความต้องการนี้สามารถครอบคลุมโดยการจัดหาวัสดุที่มีอยู่จากใบสั่งซื้อที่ยืนยันแล้วต่อไปนี้:

- **PO1:** วันที่รับสินค้า = วันนี้ + 3 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 5 วัน

เนื่องจากระบบได้รับการตั้งค่าคอนฟิกให้อนุญาต 10 วัน ค่าลบ จึงครอบคลุมความต้องการของ SO1 โดยการใช้ PO1 ถึงแม้ว่าผลลัพธ์จะเป็นความล่าช้าสามวัน เนื่องจาก SO1 จะสร้างสินค้าคงคลังค่าลบจนกว่า PO1 จะมาถึง ไม่มีการสร้างแผนการใบสั่งซื้อ แม้ว่าระยะเวลารอคอยสินค้าจะเป็น 0 (ศูนย์) และการสร้างแผนการใบสั่งซื้อจะลดความล่าช้า

ตารางต่อไปนี้สรุปผลลัพธ์

| ความต้องการ | การเชื่อมโยงความต้องการกับการจัดซื้อ |
|---|---|
| **SO1:** วันที่จัดส่ง = วันนี้, ปริมาณ = 1 | **PO1:** วันที่รับสินค้า = วันนี้ + 3 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 5 วัน |

ภาพประกอบต่อไปนี้แสดงเส้นเวลาสำหรับตัวอย่างนี้

![ตัวอย่างที่ 5: Simple FEFO ความต้องการ, 10 วันที่ติดลบ](media/fefo-example-5.png "ตัวอย่างที่ 5: Simple FEFO ความต้องการ, 10 วันที่ติดลบ")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>ตัวอย่างที่ 6: Simple FEFO ความต้องการ, ห้าวันที่ติดลบ

ตัวอย่างนี้แสดงวิธีการทำงานของอายุการเก็บสินค้า เมื่อจำนวนวันที่ติดลบสำหรับสินค้าน้อยกว่าระยะเวลาอายุการเก็บสินค้า

ระบบมีการตั้งค่าสินค้าและแผนหลักต่อไปนี้:

- **รหัสความครอบคลุม (กลยุทธ์การเติมสินค้า):** ความต้องการ
- **วันที่ขายได้:** 0 วัน
- **ระยะเวลารอคอยสินค้า:** 0 วัน
- **จำนวนวันค่าลบ:** 5 วัน
- **ชนิดของแผนการใบสั่ง (การตั้งค่าใบสั่งเริ่มต้นของสินค้า):** ใบสั่งซื้อ

ใบสั่งขายต่อไปนี้มีอยู่ในระบบ

- **SO1:** ปริมาณ = 2, วันที่จัดส่งที่ร้องขอ = วันนี้

ความต้องการนี้สามารถครอบคลุมโดยการจัดหาวัสดุที่มีอยู่จากใบสั่งซื้อที่ยืนยันแล้วต่อไปนี้:

- **PO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 1 วัน
- **PO2:** วันที่รับสินค้า = วันนี้ + 2 วัน, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 3 วัน

อย่างไรก็ตาม ระบบต้องยอมรับข้อจํากัดว่าสินค้าที่จัดส่งไม่สามารถหมดอายุได้ในเวลาที่จัดส่งสินค้า ดังนั้น PO2 และ PO1 จึงไม่สามารถใช้ใน SO1 ได้ เนื่องจาก PO1 หมดอายุก่อนที่ PO2 จะมาถึง ระบบจะสร้างแผนการใบสั่งซื้อต่อไปนี้ เพื่อให้ครอบคลุมความต้องการสำหรับ SO1:

- **PPO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน

ระบบสามารถใช้ประโยชน์จากวันที่ติดลบห้าวัน และใช้ PO2 และ PPO1 เพื่อครอบคลุม SO1 อย่างไรก็ตาม วิธีการนี้จะทําให้การจัดส่งล่าช้าจนกว่า PO2 จะมาถึง และ PO1 จะหมดอายุในระหว่างนี้ ดังนั้น ระบบจึงครอบคลุม SO1 โดยการใช้ PPO1 และ PO1

ตารางต่อไปนี้สรุปผลลัพธ์

| ความต้องการ | การเชื่อมโยงความต้องการกับการจัดซื้อ |
|---|---|
| **SO1:** วันที่จัดส่ง = วันนี้, ปริมาณ = 2 | <p>**PO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 1 วัน</p><p>**PPO1:** วันที่รับสินค้า = วันนี้, ปริมาณ = 1, วันหมดอายุ = วันนี้ + 10 วัน</p> |

ภาพประกอบต่อไปนี้แสดงเส้นเวลาสำหรับตัวอย่างนี้

![ตัวอย่างที่ 6: Simple FEFO ความต้องการ, ห้าวันที่ติดลบ](media/fefo-example-6.png "ตัวอย่างที่ 6: Simple FEFO ความต้องการ, ห้าวันที่ติดลบ")
