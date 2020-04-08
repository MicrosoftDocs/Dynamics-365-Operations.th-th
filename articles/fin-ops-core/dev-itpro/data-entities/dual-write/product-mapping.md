---
title: ประสบการณ์ผลิตภัณฑ์โดยรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลผลิตภัณฑ์ระหว่างแอป Finance and Operations และ Common Data Service
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7de7af1084b62a7248eeda54df215e56f2541286
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173211"
---
# <a name="unified-product-experience"></a>ประสบการณ์ใช้งานผลิตภัณฑ์แบบครบวงจร

[!include [banner](../../includes/banner.md)]



เมื่อระบบนิเวศทางธุรกิจถูกสร้างขึ้นจากแอป Dynamics 365 เช่น Finance Supply Chain Management และ Sales บ่อยครั้งที่หน่ายงานธุรกิจจะใช้แอปเหล่านี้เพื่อค้นหาข้อมูลผลิตภัณฑ์ ทั้งนี้เนื่องจากแอปเหล่านี้แสดงโครงสร้างพื้นฐานของผลิตภัณฑ์ที่แข็งแกร่ง พร้อมกับแนวคิดการกำหนดราคาที่ซับซ้อนและข้อมูลปริมาณคงคลังคงเหลือที่ถูกต้อง หน่วยงานธุรกิจที่ใช้ระบบการจัดการรอบการขายของผลิตภัณฑ์ (PLM) สำหรับการค้นหาข้อมูลผลิตภัณฑ์ สามารถนำผลิตภัณฑ์จากแอป Finance and Operations ไปยังแอป Dynamics 365 อื่นๆได้ ประสบการณ์ใช้งานผลิตภัณฑ์โดยรวมจะนำแบบจำลองข้อมูลผลิตภัณฑ์รวมเข้าใน Common Data Service เพื่อให้ผู้ใช้แอปทั้งหมด รวมทั้งผู้ใช้ Power Platform สามารถใช้ประโยชน์จากข้อมูลผลิตภัณฑ์จำนวนมากที่มาจากแอป Finance and Operations

นี่คือแบบจำลองข้อมูลผลิตภัณฑ์จาก Sales

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์ ใน CE](media/dual-write-product-4.jpg)

นี่คือแบบจำลองข้อมูลผลิตภัณฑ์จากแอป Finance and Operations

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์ ใน Finance and Operations](media/dual-write-products-5.jpg)

แบบจำลองข้อมูลผลิตภัณฑ์สองแบบนี้ได้รวมอยู่ใน Common Data Service ตามที่แสดงด้านล่าง

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์ในแอป Dynamics 365](media/dual-write-products-6.jpg)

แผนผังเอนทิตี้แบบการเขียนแบบคู่สำหรับผลิตภัณฑ์ที่ได้รับการออกแบบมาเพื่อส่งผ่านข้อมูลทางเดียวเท่านั้น ในประสบการณ์แบบใกล้เวลาจริงจากแอป Finance and Operations ไปที่ Common Data Service อย่างไรก็ตาม โครงสร้างพื้นฐานของผลิตภัณฑ์ถูกสร้างแบบเปิดเพื่อทำให้เป็นสองทิศทาง เมื่อจำเป็น แม้ว่าคุณจะสามารถกำหนดเองได้ ที่เป็นความเสี่ยงของคุณเอง เนื่องจาก Microsoft ไม่แนะนำวิธีการนี้

## <a name="templates"></a>เท็มเพลต

ข้อมูลผลิตภัณฑ์ ประกอบด้วยข้อมูลทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ และคำนิยามของผลิตภัณฑ์ เช่น มิติของผลิตภัณฑ์ หรือการติดตาม และมิติการจัดเก็บ ดังที่ตารางต่อไปนี้แสดง ชุดข้อมูลของแผนผังเอนทิตี้ถูกสร้างเพื่อซิงค์ผลิตภัณฑ์และข้อมูลที่เกี่ยวข้อง

แอป Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365 | คำอธิบาย
-----------------------|--------------------------------|---
ผลิตภัณฑ์ที่นำออกใช้ V2 | msdyn\_sharedproductdetails | เอนทิตี้ **msdyn\_sharedproductdetails** ประกอบด้วยฟิลด์จากแอป Finance and Operations ที่กำหนดผลิตภัณฑ์และมีข้อมูลทางการเงินและการจัดการของผลิตภัณฑ์ 
Common Data Service ผลิตภัณฑ์เฉพาะที่นำออกใช้ | ผลิตภัณฑ์ | เอนทิตี้ **ผลิตภัณฑ์** ประกอบด้วยฟิลด์ที่กำหนดผลิตภัณฑ์ โดยรวมถึงผลิตภัณฑ์แต่ละรายการ (ผลิตภัณฑ์ที่มีผลิตภัณฑ์ชนิดย่อย) และผลิตภัณฑ์ย่อย ตารางต่อไปนี้แสดงการแม็ป
บาร์โค้ดที่ระบุหมายเลขผลิตภัณฑ์ | msdyn\_productbarcodes | บาร์โคดของผลิตภัณฑ์ถูกใช้เพื่อระบุผลิตภัณฑ์โดยไม่ซ้ำ
การตั้งค่าใบสั่งเริ่มต้น | msdyn\_productdefaultordersettings
การตั้งค่าใบสั่งเริ่มต้นโดยเฉพาะของผลิตภัณฑ์ | msdyn_productdefaultordersettings
กลุ่มมิติของผลิตภัณฑ์ | msdyn\_productdimensiongroups | กลุ่มมิติของผลิตภัณฑ์ที่กำหนดว่ามิติของผลิตภัณฑ์ใดที่กำหนดผลิตภัณฑ์ 
กลุ่มมิติการจัดเก็บ | msdyn\_productstoragedimensiongroups | กลุ่มมิติของการจัดเก็บผลิตภัณฑ์แสดงวิธีการที่ใช้กำหนดการจัดวางผลิตภัณฑ์ในคลังสินค้า
กลุ่มมิติการติดตาม | msdyn\_producttrackingdimensiongroups | กลุ่มมิติของการติดตามผลิตภัณฑ์แสดงวิธีการที่ใช้ในการติดตามผลิตภัณฑ์ในสินค้าคงคลัง
สี | msdyn\_productcolors
ขนาด | msdyn\_productsizes
ลักษณะ | msdyn\_productsytles
การตั้งค่าคอนฟิก | msdyn\_productconfigurations
สีของผลิตภัณฑ์หลัก | msdyn_sharedproductcolors | เอนทิตี้ **สีผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้สีที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน
ขนาดของผลิตภัณฑ์หลัก | msdyn_sharedproductsizes | เอนทิตี้ **ขนาดผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้ขนาดที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน
ลักษณะของผลิตภัณฑ์หลัก | msdyn_sharedproductstyles | เอนทิตี้ **ลักษณะผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้ลักษณะที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน
การตั้งค่าคอนฟิกผลิตภัณฑ์หลัก | msdyn_sharedproductconfigurations | เอนทิตี้ **การตั้งค่าคอนฟิกของผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้การตั้งค่าคอนฟิกที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน
ผลิตภัณฑ์ทั้งหมด | msdyn_globalproducts | เอนทิตี้ผลิตภัณฑ์ทั้งหมดมีผลิตภัณฑ์ทั้งหมดที่มีอยู่ในแอป Finance and Operations ทั้งผลิตภัณฑ์ที่นำออกใช้และผลิตภัณฑ์ที่ไม่ได้นำออกใช้
หน่วย | uoms
การแปลงหน่วย | msdyn_ unitofmeasureconversions
การแปลงหน่วยวัดเฉพาะของผลิตภัณฑ์ | msdyn_productspecificunitofmeasureconversion
ประเภทผลิตภัณฑ์ | msdyn_productcategories | แต่ละประเภทผลิตภัณฑ์และข้อมูลเกี่ยวกับโครงสร้างและลักษณะของผลิตภัณฑ์มีอยู่ในเอนทิตี้ประเภทผลิตภัณฑ์ 
การจัดประเภทตามลำดับชั้นของผลิตภัณฑ์ | msdyn_productcategoryhierarhies | คุณใช้ลำดับชั้นของผลิตภัณฑ์เพื่อจัดประเภทหรือจัดกลุ่มผลิตภัณฑ์ ลำดับชั้นประเภทพร้อมใช้งานใน Common Data Service โดยใช้เอนทิตี้ลำดับชั้นประเภทของผลิตภัณฑ์ 
บทบาทการจัดประเภทตามลำดับชั้นของผลิตภัณฑ์ | msdyn_productcategoryhierarchies | ลำดับชั้นของผลิตภัณฑ์สามารถใช้สำหรับบทบาทต่างๆ ใน D365 Finance and Operations จะมีการระบุประเภทที่ใช้ในแต่ละบทบาทที่มีการใช้เอนทิตี้บทบาทประเภทของผลิตภัณฑ์ 
การกำหนดประเภทผลิตภัณฑ์ | msdyn_productcategoryassignments | เมื่อต้องการกำหนดผลิตภัณฑ์ให้กับประเภทที่สามารถใช้เอนทิตี้การกำหนดประเภทผลิตภัณฑ์

## <a name="integration-of-products"></a>การรวมของผลิตภัณฑ์

ในแบบจำลองนี้ ผลิตภัณฑ์จะแสดงด้วยเอนทิตี้สองชุดใน Common Data Service: **ผลิตภัณฑ์** และ **msdyn\_sharedproductdetails** ในขณะที่เอนทิตี้แรกประกอบด้วยคำนิยามของผลิตภัณฑ์ (ตัวระบุเฉพาะสำหรับ ผลิตภัณฑ์ ชื่อผลิตภัณฑ์ และคำอธิบาย) เอนทิตี้ที่สองประกอบด้วยฟิลด์ที่จัดเก็บอยู่ในระดับผลิตภัณฑ์ การรวมกันของสองเอนทิตี้เหล่านี้จะใช้ในการกำหนดผลิตภัณฑ์ตามแนวคิดของหน่วยการเก็บสต็อกสินค้า (SKU) ผลิตภัณฑ์ที่นำออกใช้แต่ละรายการจะมีข้อมูลอยู่ในเอนทิตี้ดังกล่าว (ผลิตภัณฑ์และรายละเอียดผลิตภัณฑ์ที่ใช้ร่วมกัน) เพื่อติดตามผลิตภัณฑ์ทั้งหมด (ที่นำออกใช้และไม่นำออกใช้) เอนทิตี **ผลิตภัณฑ์สากล** จะถูกนำมาใช้ 

เนื่องจากผลิตภัณฑ์แสดงเป็น SKU แนวคิดของผลิตภัณฑ์ที่แตกต่างกัน ผลิตภัณฑ์หลัก และผลิตภัณฑ์ย่อยสามารถจับภาพได้ใน Common Data Service ในลักษณะต่อไปนี้:

- **ผลิตภัณฑ์ที่มีผลิตภัณฑ์ชนิดย่อย** คือผลิตภัณฑ์ที่กำหนดโดยตัวเอง ไม่จำเป็นต้องกำหนดมิติ ตัวอย่างคือสมุดบัญชีเฉพาะ สำหรับผลิตภัณฑ์เหล่านี้ มีการสร้างเรกคอร์ดหนึ่งรายการในเอนทิตี้ **ผลิตภัณฑ์** และมีการสร้างเรกคอร์ดหนึ่งรายการในเอนทิตี้ **msdyn\_haredproductdetails** ไม่มีการสร้างเรกคอร์ดตระกูลผลิตภัณฑ์
- **ผลิตภัณฑ์หลัก** จะใช้เป็นผลิตภัณฑ์ทั่วไปที่มีคำนิยามและกฎที่กำหนดลักษณะการทำงานในกระบวนการทางธุรกิจ โดยขึ้นอยู่กับข้อกำหนดเหล่านี้ ผลิตภัณฑ์เฉพาะที่ถูกเรียกว่าผลิตภัณฑ์ย่อยสามารถสร้างขึ้นตามข้อกำหนดเหล่านี้ได้ ตัวอย่างเช่น เสื้อยืดเป็นผลิตภัณฑ์หลัก และสามารถมีสีและขนาดเป็นมิติได้ ผลิตภัณฑ์ย่อยสามารถนำออกใช้โดยมีการรวมกันของมิติเหล่านี้ เช่น เสื้อสีน้ำเงินขนาดเล็ก หรือเสื้อยืดสีเขียวขนาดกลาง ในการรวม หนึ่งเรกคอร์ดต่อผลิตภัณฑ์ย่อยจะถูกสร้างขึ้นในตารางผลิตภัณฑ์ เรกคอร์ดนี้มีข้อมูลเฉพาะตัวของตัวแปร เช่น มิติต่างๆ ข้อมูลทั่วไปสำหรับผลิตภัณฑ์ถูกจัดเก็บไว้ในเอนทิตี้ **msdyn\_sharedproductdetails** (ข้อมูลทั่วไปนี้จะจัดเก็บอยู่ในผลิตภัณฑ์หลัก) นอกจากนี้มีการสร้างเรกคอร์ดตระกูลผลิตภัณฑ์หนึ่งรายการต่อผลิตภัณฑ์หลัก ข้อมูลของผลิตภัณฑ์หลักจะถูกซิงค์กับ Common Data Service ทันทีที่มีการสร้างผลิตภัณฑ์หลักที่นำออกใช้ (แต่ก่อนที่ผลิตภัณฑ์ย่อยจะนำออกใช้)
- **ผลิตภัณฑ์เฉพาะ** อ้างอิงถึงผลิตภัณฑ์ชนิดย่อยของผลิตภัณฑ์ทั้งหมดและผลิตภัณฑ์ย่อยทั้งหมด 

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์](media/dual-write-product.png)

เมื่อฟังก์ชันการเขียนแบบคู่ถูกเปิดใช้งาน แอปจาก Finance and Operations จะได้รับการซิงค์ในแอป Dynamics 365 อื่นในสถานะ **ร่าง** มีการเพิ่มที่รายการราคาแรกที่มีสกุลเงินเดียวกัน กล่าวอีกอย่างหนึ่งคือมีการเพิ่มรายการราคาแรกในแอพลิเคชัน Dynamics 365 ซึ่งตรงกับสกุลเงินของนิติบุคคลที่มีการนำผลิตภัณฑ์ออกใช้ในแอป Finance and Operations 

โดยผลิตภัณฑ์เริ่มต้นจากแอป Finance and Operations จะถูกซิงโครไนส์กับแอป Dynamics 365 อื่นๆ ในสถานะ **แบบร่าง** ถ้าต้องการซิงค์ผลิตภัณฑ์กับสถานะ **ที่ใช้งานอยู่** เพื่อใ้ห้คุณสามารถใช้การตั้งค่าต่อไปนี้ในใบเสนอราคาของใบสั่งขายได้โดยตรง ตัวอย่างเช่น การตั้งค่าต่อไปนี้จำเป็นต้องมีการเลือก ภายใต้: แท็บ **ระบบ > การจัดการ > ระบบการจัดการ > การตั้งค่าระบบ > การขาย** และเลือก **สร้างผลิตภัณฑ์ในสถานะที่ใช้งานอยู่ = ใช่** 

โปรดทราบว่าการซิงโครไนส์ผลิตภัณฑ์เกิดขึ้นจากแอป Finance and Operations ไปยัง Common Data Service ซึ่งหมายความว่าค่าของฟิลด์เอนทิตี้ของผลิตภัณฑ์สามารถเปลี่ยนได้ ใน Common Data Service แต่เมื่อการซิงโครไนส์ถูกทริกเกอร์ (เมื่อมีการปรับเปลี่ยนฟิลด์ของผลิตภัณฑ์ในแอป Finance and Operations) ซึ่งจะเขียนทับค่าใน Common Data Service 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>มิติของผลิตภัณฑ์ 

มิติของผลิตภัณฑ์คือลักษณะที่ระบุผลิตภัณฑ์ย่อย นอกจากนี้ยังมีการแม็ปมิติของผลิตภัณฑ์สี่มิติ (สี ขนาด ลักษณะ และการตั้งค่าคอนฟิก) ไปที่ Common Data Service เพื่อกำหนดผลิตภัณฑ์ย่อย แผนภาพต่อไปนี้แสดงแบบจำลองข้อมูลสำหรับสีของมิติของผลิตภัณฑ์ แบบจำลองเดียวกันจะถูกนำไปใช้กับขนาด ลักษณะ และการตั้งค่าคอนฟิก 

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

เมื่อผลิตภัณฑ์มีมิติของผลิตภัณฑ์แตกต่างกัน (ตัวอย่างเช่น ผลิตภัณฑ์หลักมีขนาด และสีเป็นมิติของผลิตภัณฑ์) แต่ละผลิตภัณฑ์เฉพาะ (คือ ผลิตภัณฑ์ย่อยแต่ละรายการ) จะถูกกำหนดเป็นชุดของมิติของผลิตภัณฑ์ดังกล่าว ตัวอย่างเช่น หมายเลขผลิตภัณฑ์ B0001 เป็นเสื้อยืดสีดำขนาดเล็กพิเศษ และหมายเลขผลิตภัณฑ์ B0002 เป็นเสื้อยืดสีดำขนาดเล็ก ในกรณีนี้ จะมีการกำหนดชุดของมิติของผลิตภัณฑ์ที่มีอยู่ ตัวอย่างเช่น เสื้อยืดจากตัวอย่างก่อนหน้านี้อาจมีขนาดเล็กเป็นพิเศษและสีดำ ขนาดเล็กและสีดำ ขนาดกลางและสีดำ หรือขนาดใหญ่และสีดำ แต่ไม่สามารถเป็นใหญ่เป็นพิเศษและสีดำได้ กล่าวอีกอย่างหนึ่งคือ มีการระบุมิติของผลิตภัณฑ์ที่ผลิตภัณฑ์หลักสามารถใช้ได้ และสามารถนำผลิตภัณฑ์ย่อยออกใช้ตามค่าเหล่านี้ได้

เมื่อต้องการติดตามมิติของผลิตภัณฑ์ที่ผลิตภัณฑ์หลักสามารถใช้ได้ จะมีการสร้างและแม็ปเอนทิตี้ต่อไปนี้ใน Common Data Service สำหรับแต่ละมิติของผลิตภัณฑ์ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมข้อมูลผลิตภัณฑ์](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information)

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>การตั้งค่าใบสั่งเริ่มต้นและการตั้งค่าใบสั่งเริ่มต้นเฉพาะผลิตภัณฑ์

การตั้งค่าใบสั่งเริ่มต้นกำหนดไซต์และคลังสินค้าที่สินค้าจะเป็นต้นทางหรือจัดเก็บ ปริมาณต่ำสุด สูงสุด หลายรายการ และมาตรฐานที่จะใช้สำหรับการค้าหรือการจัดการสินค้าคงคลัง ระยะเวลารอคอยสินค้า แฟล็กหยุด และวิธีการสัญญาว่าจะออกใบสั่ง ข้อมูลนี้พร้อมใช้งานใน Common Data Service โดยใช้การตั้งค่าใบสั่งเริ่มต้นและเอนทิตี้การตั้งค่าใบสั่งเริ่มต้นเฉพาะผลิตภัณฑ์ คุณสามารถอ่านข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันใน [หัวข้้อการตั้งค่าใบสั่งเริ่มต้น](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings)

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>หน่วยวัดและการแปลงหน่วยวัด

หน่วยวัดและการแปลงที่เกี่ยวข้องพร้อมใช้งานใน Common Data Service ตามแบบจำลองข้อมูลที่แสดงในแผนภาพ

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์](media/dual-write-product-three.png)

แนวคิดหน่วยวัดถูกรวมกันระหว่างแอป Finance and Operations และแอปอื่นๆของ Dynamics 365 สำหรับประเภทของหน่วยแต่ละประเภทในแอป Finance and Operations กลุ่มหน่วยจะถูกสร้างขึ้นในแอป Dynamics 365 ซึ่งประกอบด้วยหน่วยที่อยู่ในประเภทของหน่วย นอกจากนี้ยังมีการสร้างหน่วยพื้นฐานเริ่มต้นสำหรับทุกกลุ่มหน่วยด้วย 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>การซิงโครไนส์ครั้งแรกของการตรงกันของข้อมูลหน่วยระหว่าง Finance and Operations และ Common Data Service

### <a name="initial-synchronization-of-units"></a>การซิงโครไนส์เริ่มแรกของหน่วย

เมื่อการเขียนแบบคู่ถูกเปิดใช้งาน หน่วยจากแอป Finance and Operations จะถูกซิงโครไนส์กับแอป Dynamics 365 อื่นๆ กลุ่มของหน่วยที่ถูกซิงโครไนส์จากแอป Finance and Operations ใน Common Data Service มีการตั้งค่าแฟล็กที่บ่งชี้ว่ามีการ "เก็บรักษาไว้ภายนอก"

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>หน่วยที่ตรงกันและประเภทของหน่วย/ข้อมูลกลุ่มจากการแอป Finance and Operations และแอป Dynamics 365 อื่นๆ

ก่อนอื่น คุณจำเป็นต้องทราบว่าคีย์การรวมสำหรับหน่วยคือ msdyn_symbol ดังนั้น ค่านี้ต้องไม่ซ้ำกันใน Common Data Service หรือแอป Dynamics 365 อื่นๆ เนื่องจากในแอป Dynamics 365 อื่นๆ จะเป็นคู่ "รหัสกลุ่มของหน่วย" และ "ชื่อ" ซึ่งกำหนดเอกลักษณ์ของหน่วย คุณต้องพิจารณาสถานการณ์ต่างๆ สำหรับการจับคู่ข้อมูลหน่วยระหว่างแอป Finance and Operations และ Common Data Service

สำหรับการจับคู่หน่วย/ที่ทับซ้อนกันในแอป Finance and Operations และแอป Dynamics 365 อื่นๆ:

+ **หน่วยเป็นสมาชิกของกลุ่มหน่วยในแอป Dynamics 365 อื่นๆ ซึ่งตรงกับประเภทของหน่วยที่เชื่อมโยงในแอป Finance and Operations** ในกรณีนี้จะต้องกรอกข้อมูลในฟิลด์ msdyn_symbol ของแอป Dynamics 365 อื่นๆ ด้วยสัญลักษณ์หน่วยจากแอป Finance and Operations ดังนั้น เมื่อข้อมูลจะถูกจับคู่ และกลุ่มหน่วยจะถูกตั้งค่าเป็น "เก็บรักษาไว้ภายนอก" ในแอป Dynamics 365 อื่นๆ
+ **หน่วยเป็นสมาชิกของกลุ่มหน่วยในแอป Dynamics 365 อื่นๆ ซึ่งไม่สอดคล้องกับประเภทของหน่วยที่เชื่อมโยงในแอป Finance and Operations (ไม่มีประเภทของหน่วยที่มีอยู่ในแอป Finance and Operations สำหรับประเภทของหน่วยในแอป Dynamics 365 อื่นๆ)** ในกรณีนี้ ต้องกรอกข้อมูล msdyn_symbol โดยใช้สตริงการสุ่ม โปรดทราบว่า ค่านี้ต้องไม่ซ้ำกันในแอป Dynamics 365 อื่นๆ

สำหรับหน่วยและประเภทของหน่วยในแอป Finance and Operations ไม่มีอยู่ในแอป Dynamics 365 อื่นๆ:

ในฐานะที่เป็นส่วนหนึ่งของการรวมแบบสองทิศทาง กลุ่มหน่วยจากแอป Finance and Operations และหน่วยที่เกี่ยวข้องจะถูกสร้างขึ้นและมีการซิงโครไนส์ในแอป Dynamics 365 อื่นๆ และ Common Data Service และกลุ่มหน่วยจะถูกตั้งค่าเป็น "เก็บรักษาไว้ภายนอก" โดยที่ไม่จำเป็นต้องมีการระดมทุนเพิ่มเติม

สำหรับหน่วยในแอป Dynamics 365 อื่นๆ ที่ไม่อยู่ในแอป Finance and Operations:

ต้องกรอกข้อมูลในฟิลด์ msdyn_symbol สำหรับหน่วยทั้งหมด คุณสามารถสร้างหน่วยได้เสมอในแอป Finance and Operations ในประเภทของหน่วยที่สอดคล้องกัน (ถ้ามี) ถ้าไม่มีประเภทของหน่วยอยู่ ควรสร้างประเภทของหน่วยก่อน (โปรดทราบว่าคุณไม่สามารถสร้างประเภทของหน่วยในแอป Finance and Operations ยกเว้นผ่านส่วนขยาย ถ้าคุณกำลังขยาย enum) ที่จับคู่กับกลุ่มหน่วยของแอป Dynamics 365 อื่นๆ จากนั้น คุณจะสามารถสร้างหน่วยได้ โปรดทราบว่าสัญลักษณ์หน่วยในแอป Finance and Operations ต้องเป็น msdyn_symbol ที่กำหนดไว้ก่อนหน้านี้ ในแอป Dynamics 365 อื่นๆ สำหรับหน่วย

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>นโยบายผลิตภัณฑ์ คือ มิติ การติดตาม และกลุ่มการจัดเก็บ

นโยบายผลิตภัณฑ์เป็นชุดของนโยบายที่ใช้สำหรับการกำหนดผลิตภัณฑ์และลักษณะของสินค้าในสินค้าคงคลัง กลุ่มมิติของผลิตภัณฑ์ กลุ่มมิติการติดตามของผลิตภัณฑ์ และกลุ่มมิติการจัดเก็บสามารถพบได้เป็นนโยบายผลิตภัณฑ์ 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>ลำดับขั้นผลิตภัณฑ์

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>คีย์การรวมสำหรับผลิตภัณฑ์ 

เมื่อต้องการระบุผลิตภัณฑ์ ระหว่าง Dynamics 365 for Finance and Operations และผลิตภัณฑ์ใน Common Data Service คีย์การรวมโดยเฉพาะ สำหรับผลิตภัณฑ์ **(productnumber)** เป็นคีย์เฉพาะที่ระบุผลิตภัณฑ์ใน Common Data Service ซึ่งประกอบด้วยการเรียงต่อกันของ: **(company, msdyn_productnumber)** **บริษัท** บ่งชี้ถึงนิติบุคคลใน Finance and Operations และ **msdyn_productnumber** บ่งชี้หมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ที่ระบุใน Finance and Operations 

สำหรับผู้ใช้ของแอป Dynamics 365 อื่นๆ ผลิตภัณฑ์จะถูกระบุใน UI ด้วย **msdyn_productnumber** (หมายเหตุว่า ป้ายชื่อของฟิลด์คือ **หมายเลขผลิตภัณฑ์**) ในฟอร์มผลิตภัณฑ์ ทั้งบริษัทและ msydn_productnumber จะแสดงขึ้น อย่างไรก็ตาม ฟิลด์ (productnumber) คีย์เฉพาะสำหรับผลิตภัณฑ์จะไม่แสดงขึ้น 

ถ้าคุณสร้างแอปบน Common Data Service คุณควรให้ความสำคัญกับการใช้ **productnumber** (รหัสเฉพาะของผลิตภัณฑ์) เป็นคีย์การรวม อย่าใช้ **msdyn_productnumber** เนื่องจากไม่มีเอกลักษณ์เฉพาะ 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>การซิงโครไนส์ผลิตภัณฑ์เริ่มต้น และการย้ายข้อมูลจาก Common Data Service ไปยัง Finance and Operations

### <a name="initial-synchronization-of-products"></a>การซิงโครไนส์เริ่มแรกของผลิตภัณฑ์ 

เมื่อการเขียนแบบคู่ถูกเปิดใช้งาน ผลิตภัณฑ์จากแอป Finance and Operations จะถูกซิงโครไนส์กับ Common Data Service และแอปที่เป็นแบบโมเดลอื่นๆ ใน Dynamics 365 ผลิตภัณฑ์ที่สร้างขึ้นใน Common Data Service และแอป Dynamics 365 อื่นๆ ก่อนที่การเขียนแบบคู่ถูกนำออกใช้ จะไม่ได้รับการปรับปรุงหรือจับคู่กับข้อมูลผลิตภัณฑ์จากแอป Finance and Operations

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>ข้อมูลผลิตภัณฑ์ที่ตรงกันจาก Finance and Operations และแอป Dynamics 365 อื่นๆ

ถ้ามีการเก็บผลิตภัณฑ์เดียวกัน (ทับซ้อนกัน/ตรงกัน) ใน Finance and Operations และ Common Data Service และแอป Dynamics 365 อื่นๆ เมื่อเปิดใช้งานการเขียนแบบคู่ การซิงโครไนส์ของผลิตภัณฑ์จาก Finance and Operations จะเกิดขึ้น และเรกคอร์ดที่ซ้ำกันจะปรากฏขึ้นใน Common Data Service สำหรับผลิตภัณฑ์เดียวกัน
ถ้าต้องการหลีกเลี่ยงสถานการณ์ก่อนหน้านี้ ถ้าแอป Dynamics 365 อื่นๆ มีผลิตภัณฑ์ที่ทับซ้อนกัน/จับคู่ กับ Finance and Operations แล้วผู้ดูแลระบบจะเปิดใช้งานการเขียนแบบคู่ ต้องรีบูตฟิลด์ **บริษัท** (ตัวอย่างเช่น:"USMF") และ **msdyn_productnumber** (ตัวอย่าง: "1234:Black:S") ก่อนดำเนินการซิงโครไนซ์ของผลิตภัณฑ์ กล่าวคือ ฟิลด์เหล่านี้สองฟิลด์ในผลิตภัณฑ์ใน Common Data Service ต้องถูกกรอกข้อมูลกับบริษัทที่เกี่ยวข้องใน Finance and Operations ซึ่งผลิตภัณฑ์จำเป็นต้องตรงกับและมีหมายเลขผลิตภัณฑ์ 

หลังจากนั้น เมื่อมีการเปิดใช้งานการซิงโครไนส์ และเกิดขึ้น ผลิตภัณฑ์จาก Finance and Operations จะถูกซิงโครไนส์กับผลิตภัณฑ์ที่จับคู่ใน Common Data Service และแอป Dynamics 365 อื่นๆ ซึ่งสามารถใช้ได้กับทั้งผลิตภัณฑ์เฉพาะ และผลิตภัณฑ์ที่แตกต่างกัน 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>การรวมของข้อมูลผลิตภัณฑ์จากแอป Dynamics 365 อื่นๆไปยัง Finance and Operations

ถ้าแอป Dynamics 365 อื่นๆ มีผลิตภัณฑ์ที่ไม่มีอยู่ใน Finance and Operations ผู้ดูแลระบบสามารถใช้ **EcoResReleasedProductCreationV2Entity** สำหรับการนำเข้าผลิตภัณฑ์ดังกล่าวใน Finance and Operations ได้ก่อน และประการที่สอง ให้จับคู่ข้อมูลผลิตภัณฑ์จาก Finance and Operations และแอป Dynamics 365 อื่นๆ ดังที่อธิบายไว้ข้างต้น 
