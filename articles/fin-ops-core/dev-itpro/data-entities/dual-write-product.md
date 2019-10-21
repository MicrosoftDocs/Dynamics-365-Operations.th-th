---
title: ประสบการณ์ผลิตภัณฑ์โดยรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลผลิตภัณฑ์ระหว่างแอป Finance and Operations และ Common Data Service
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
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
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249339"
---
# <a name="unified-product-experience"></a>ประสบการณ์ผลิตภัณฑ์โดยรวม

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

เมื่อระบบนิเวศทางธุรกิจถูกสร้างขึ้นจากแอป Dynamics 365 เช่น Finance Supply Chain Management และ Sales เป็นปกติสำหรับลูกค้าที่จะใช้แอปเหล่านี้เพื่อค้นหาข้อมูลผลิตภัณฑ์ ทั้งนี้เนื่องจากแอปเหล่านี้แสดงโครงสร้างพื้นฐานของผลิตภัณฑ์ที่แข็งแกร่งพร้อมกับแนวคิดการกำหนดราคาที่ซับซ้อนและข้อมูลปริมาณคงคลังคงเหลือที่ถูกต้อง ลูกค้าที่ใช้ระบบการจัดการรอบการขายของผลิตภัณฑ์ (PLM) สำหรับการค้นหาข้อมูลผลิตภัณฑ์ สามารถนำผลิตภัณฑ์จากแอป Finance and Operations ไปยังแอป Dynamics 365 อื่นๆได้ ประสบการณ์ใช้งานผลิตภัณฑ์โดยรวมจะนำเข้าแบบจำลองข้อมูลผลิตภัณฑ์รวมไปที่ Common Data Service เพื่อให้ผู้ใช้แอปทั้งหมด รวมทั้งผู้ใช้ Power Platform สามารถใช้ประโยชน์จากข้อมูลผลิตภัณฑ์จำนวนมากที่มาจากแอป Finance and Operations

นี่คือแบบจำลองข้อมูลผลิตภัณฑ์จาก Sales

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์ Sales](media/dual-write-product-4.jpg)

นี่คือแบบจำลองข้อมูลผลิตภัณฑ์จากแอป Finance and Operations

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์ใน Finance and Operations](media/dual-write-products-5.jpg)

แบบจำลองข้อมูลผลิตภัณฑ์สองแบบนี้ได้รวมอยู่ใน Common Data Service ตามที่แสดงด้านล่าง

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์ในแอป Dynamics 365](media/dual-write-products-6.jpg)

แผนผังเอนทิตี้แบบการเขียนแบบคู่สำหรับผลิตภัณฑ์ที่ได้รับการออกแบบมาเพื่อส่งผ่านข้อมูลทางเดียวเท่านั้น และเป็นประสบการณ์แบบใกล้เวลาจริงจากแอป Finance and Operations ไปที่ Common Data Service อย่างไรก็ตาม โครงสร้างพื้นฐานของผลิตภัณฑ์ถูกสร้างแบบเปิดเพื่อทำให้เป็นสองทิศทาง เมื่อจำเป็น ลูกค้าสามารถกำหนดเองได้ด้วยความเสี่ยงของตนเอง เนื่องจาก Microsoft ไม่แนะนำวิธีการนี้

## <a name="templates"></a>เท็มเพลต

ข้อมูลผลิตภัณฑ์ประกอบด้วยข้อมูลทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์และคำนิยามของผลิตภัณฑ์ เช่น มิติของผลิตภัณฑ์ หรือการติดตาม และมิติการจัดเก็บ ดังที่ตารางต่อไปนี้แสดง ชุดข้อมูลของแผนผังเอนทิตี้ถูกสร้างเพื่อซิงค์ผลิตภัณฑ์และข้อมูลที่เกี่ยวข้อง

Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365
-----------------------|--------------------------------
ผลิตภัณฑ์ที่นำออกใช้ V2 | msdyn\_sharedproductdetails
ผลิตภัณฑ์เฉพาะที่นำออกใช้ CDS | ผลิตภัณฑ์
บาร์โค้ดที่ระบุหมายเลขผลิตภัณฑ์ | msdyn\_productbarcodes
การตั้งค่าใบสั่งเริ่มต้น | msdyn\_productdefaultordersettings
การตั้งค่าใบสั่งเริ่มต้นโดยเฉพาะของผลิตภัณฑ์ | msdyn_productspecificdefaultordersettings
กลุ่มมิติของผลิตภัณฑ์ | msdyn\_productdimensiongroups
กลุ่มมิติการจัดเก็บ | msdyn\_productstoragedimensiongroups
กลุ่มมิติการติดตาม | msdyn\_producttrackingdimensiongroups
สี | msdyn\_productcolors
ขนาด | msdyn\_productsizes
ลักษณะ | msdyn\_productsytles
การตั้งค่าคอนฟิก | msdyn\_productconfigurations
สีของผลิตภัณฑ์หลัก | msdyn_sharedproductcolors
ขนาดของผลิตภัณฑ์หลัก | msdyn_sharedproductsizes
ลักษณะของผลิตภัณฑ์หลัก | msdyn_sharedproductstyles
การตั้งค่าคอนฟิกผลิตภัณฑ์หลัก | msdyn_sharedproductconfigurations
ผลิตภัณฑ์ทั้งหมด | msdyn_globalproducts
หน่วย | uoms
การแปลงหน่วย | msdyn_ unitofmeasureconversions
การแปลงหน่วยวัดเฉพาะของผลิตภัณฑ์ | msdyn_productspecificunitofmeasureconversion
ไซต์ | msdyn\_operationalsites
คลังสินค้า | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>การรวมของผลิตภัณฑ์

ในแบบจำลองนี้ ผลิตภัณฑ์จะแสดงด้วยเอนทิตี้สองชุดใน Common Data Service: **ผลิตภัณฑ์** และ **msdyn\_sharedproductdetails** ในขณะที่เอนทิตี้แรกประกอบด้วยคำนิยามของผลิตภัณฑ์ (ตัวระบุเฉพาะสำหรับผลิตภัณฑ์ ชื่อผลิตภัณฑ์ และคำอธิบาย) เอนทิตี้ที่สองประกอบด้วยฟิลด์ที่จัดเก็บอยู่ในระดับผลิตภัณฑ์ การรวมกันของสองเอนทิตี้เหล่านี้จะใช้ในการกำหนดผลิตภัณฑ์ตามแนวคิดของหน่วยการเก็บสต็อกสินค้า (SKU) ผลิตภัณฑ์ที่นำออกใช้แต่ละรายการจะมีข้อมูลอยู่ในเอนทิตี้ดังกล่าว (ผลิตภัณฑ์และรายละเอียดผลิตภัณฑ์ที่ใช้ร่วมกัน) เพื่อติดตามผลิตภัณฑ์ทั้งหมด (ที่นำออกใช้และไม่นำออกใช้) **ผลิตภัณฑ์สากล** จะถูกนำมาใช้ 

เนื่องจากผลิตภัณฑ์แสดงเป็น SKU แนวคิดของผลิตภัณฑ์ที่แตกต่างกัน ผลิตภัณฑ์หลัก และผลิตภัณฑ์ย่อยสามารถจับภาพได้ใน Common Data Service ในลักษณะต่อไปนี้:

- **ผลิตภัณฑ์ที่มีผลิตภัณฑ์ชนิดย่อย** คือผลิตภัณฑ์ที่กำหนดโดยตัวเอง ไม่จำเป็นต้องกำหนดมิติ ตัวอย่างคือสมุดบัญชีเฉพาะ สำหรับผลิตภัณฑ์เหล่านี้ มีการสร้างเรกคอร์ดหนึ่งรายการในเอนทิตี้ **ผลิตภัณฑ์** และมีการสร้างเรกคอร์ดหนึ่งรายการในเอนทิตี้ **msdyn\_haredproductdetails** ไม่มีการสร้างเรกคอร์ดตระกูลผลิตภัณฑ์
- **ผลิตภัณฑ์หลัก** จะใช้เป็นผลิตภัณฑ์ทั่วไปที่มีคำนิยามและกฎที่กำหนดลักษณะการทำงานในกระบวนการทางธุรกิจ โดยขึ้นอยู่กับข้อกำหนดเหล่านี้ ผลิตภัณฑ์เฉพาะที่ถูกเรียกว่าผลิตภัณฑ์ย่อยสามารถสร้างขึ้นตามข้อกำหนดเหล่านี้ได้ ตัวอย่างเช่น เสื้อยืดเป็นผลิตภัณฑ์หลัก และสามารถมีสีและขนาดเป็นมิติได้ ผลิตภัณฑ์ย่อยสามารถนำออกใช้โดยมีการรวมกันของมิติเหล่านี้ เช่น เสื้อสีน้ำเงินขนาดเล็ก หรือเสื้อยืดสีเขียวขนาดกลาง ในการรวม หนึ่งเรกคอร์ดต่อผลิตภัณฑ์ย่อยจะถูกสร้างขึ้นในตารางผลิตภัณฑ์ เรกคอร์ดนี้มีข้อมูลเฉพาะตัวของตัวแปร เช่น มิติต่างๆ ข้อมูลทั่วไปสำหรับผลิตภัณฑ์ถูกจัดเก็บไว้ในเอนทิตี้ **msdyn\_sharedproductdetails** (ข้อมูลทั่วไปนี้จะจัดเก็บอยู่ในผลิตภัณฑ์หลัก) นอกจากนี้มีการสร้างเรกคอร์ดตระกูลผลิตภัณฑ์หนึ่งรายการต่อผลิตภัณฑ์หลัก ข้อมูลของผลิตภัณฑ์หลักจะถูกซิงค์กับ Common Data Service ทันทีที่มีการสร้างผลิตภัณฑ์หลักที่นำออกใช้ (แต่ก่อนที่ผลิตภัณฑ์ย่อยจะนำออกใช้)
- **ผลิตภัณฑ์เฉพาะ** อ้างอิงถึงผลิตภัณฑ์ชนิดย่อยของผลิตภัณฑ์ทั้งหมดและผลิตภัณฑ์ย่อยทั้งหมด 

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์](media/dual-write-product.png)

เมื่อฟังก์ชันการเขียนแบบคู่เปิดใช้งาน แอปจาก Finance and Operations จะได้รับการซิงค์ในแอป Dynamics 365 อื่นในสถานะ **ร่าง** มีการเพิ่มที่รายการราคาแรกที่มีสกุลเงินเดียวกัน กล่าวอีกอย่างหนึ่งคือมีการเพิ่มรายการราคาแรกในแอพลิเคชัน Dynamics 365 ซึ่งตรงกับสกุลเงินของนิติบุคคลที่มีการนำผลิตภัณฑ์ออกใช้ในแอป Finance and Operations 

ถ้าต้องการซิงค์ผลิตภัณฑ์กับสถานะ **ที่ใช้งานอยู่** คุณสามารถใช้การตั้งค่าต่อไปนี้ในใบเสนอราคาของใบสั่งขายได้โดยตรง ตัวอย่างเช่น การตั้งค่าต่อไปนี้จำเป็นต้องมีการเลือก ภายใต้ **ระบบ > การจัดการ > ระบบการจัดการ > การตั้งค่าระบบ > การขาย** เลือก **สร้างผลิตภัณฑ์ในสถานะที่ใช้งานอยู่ = ตกลง** 

### <a name="cds-released-distinct-products-to-product"></a>CDS นำผลิตภัณฑ์เฉพาะออกใช้ให้กับผลิตภัณฑ์

เอนทิตี้ **ผลิตภัณฑ์** ประกอบด้วยฟิลด์ที่กำหนดผลิตภัณฑ์ โดยรวมถึงผลิตภัณฑ์แต่ละรายการ (ผลิตภัณฑ์ที่มีผลิตภัณฑ์ชนิดย่อย) และผลิตภัณฑ์ย่อย ตารางต่อไปนี้แสดงการแม็ป

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | name
PRODUCTDESCRIPTION | >> | คำอธิบาย
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | price / ราคา
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>ดันผลิตภัณฑ์ V2 ออกไปยัง msdyn\_sharedproductdetails

เอนทิตี้ **Msdyn\_sharedproductdetails** ประกอบด้วยฟิลด์จากแอป Finance and Operations ที่กำหนดผลิตภัณฑ์และมีข้อมูลทางการเงินและการจัดการของผลิตภัณฑ์ ตารางต่อไปนี้แสดงการแม็ป

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>ผลิตภัณฑ์ทั้งหมดไปที่ผลิตภัณฑ์ msdyn_global

เอนทิตี้ผลิตภัณฑ์ทั้งหมดมีผลิตภัณฑ์ทั้งหมดที่มีอยู่ในแอป Finance and Operations ทั้งผลิตภัณฑ์ที่นำออกใช้และผลิตภัณฑ์ที่ไม่ได้นำออกใช้ ผลิตภัณฑ์เหล่านี้พร้อมใช้งานใน Common Data Service โดยใช้การแม็ปดังต่อไปนี้

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>มิติของผลิตภัณฑ์ 

มิติของผลิตภัณฑ์คือลักษณะที่ระบุผลิตภัณฑ์ย่อย นอกจากนี้ยังมีการแม็ปมิติของผลิตภัณฑ์สี่มิติ (สี ขนาด ลักษณะ และการตั้งค่าคอนฟิก) ไปที่ Common Data Service เพื่อกำหนดผลิตภัณฑ์ย่อย แผนภาพต่อไปนี้แสดงแบบจำลองข้อมูลสำหรับสีของมิติของผลิตภัณฑ์ แบบจำลองเดียวกันจะถูกนำไปใช้กับขนาด ลักษณะ และการตั้งค่าคอนฟิก 

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์](media/dual-write-product-2.PNG)

### <a name="colors"></a>สี

สีที่เป็นไปได้สามารถใช้ได้ใน Common Data Service ผ่านการแม็ปดังต่อไปนี้

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>ขนาด

ขนาดที่เป็นไปได้สามารถใช้ได้ใน Common Data Service ผ่านการแม็ปดังต่อไปนี้

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>ลักษณะ

ลักษณะที่เป็นไปได้สามารถใช้ได้ใน Common Data Service ผ่านการแม็ปดังต่อไปนี้

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>การตั้งค่าคอนฟิก

การตั้งค่าคอนฟิกที่เป็นไปได้สามารถใช้ได้ใน Common Data Service ผ่านการแม็ปดังต่อไปนี้

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
CONFIGURATIONID | \>\> | msdyn\_name

เมื่อผลิตภัณฑ์มีมิติของผลิตภัณฑ์แตกต่างกัน (ตัวอย่างเช่น ผลิตภัณฑ์หลักมีขนาด และสีเป็นมิติของผลิตภัณฑ์) แต่ละผลิตภัณฑ์เฉพาะ (คือ ผลิตภัณฑ์ย่อยแต่ละรายการ) จะถูกกำหนดเป็นชุดของมิติของผลิตภัณฑ์ดังกล่าว ตัวอย่างเช่น หมายเลขผลิตภัณฑ์ B0001 เป็นเสื้อยืดสีดำขนาดเล็กพิเศษ และหมายเลขผลิตภัณฑ์ B0002 เป็นเสื้อยืดสีดำขนาดเล็ก ในกรณีนี้ จะมีการกำหนดชุดของมิติของผลิตภัณฑ์ที่มีอยู่ ตัวอย่างเช่น เสื้อยืดจากตัวอย่างก่อนหน้านี้อาจมีขนาดเล็กเป็นพิเศษและสีดำ ขนาดเล็กและสีดำ ขนาดกลางและสีดำ หรือขนาดใหญ่และสีดำ แต่ไม่สามารถเป็นใหญ่เป็นพิเศษและสีดำได้ กล่าวอีกอย่างหนึ่งคือ มีการระบุมิติของผลิตภัณฑ์ที่ผลิตภัณฑ์หลักสามารถใช้ได้ และสามารถนำผลิตภัณฑ์ย่อยออกใช้ตามค่าเหล่านี้ได้

เมื่อต้องการติดตามมิติของผลิตภัณฑ์ที่ผลิตภัณฑ์หลักสามารถใช้ได้ จะมีการสร้างและแม็ปเอนทิตี้ต่อไปนี้ใน Common Data Service สำหรับแต่ละมิติของผลิตภัณฑ์ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมข้อมูลผลิตภัณฑ์](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information)

### <a name="shared-product-color"></a>สีผลิตภัณฑ์ที่ใช้ร่วมกัน

เอนทิตี้ **สีผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้สีที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน ตารางต่อไปนี้แสดงการแม็ป

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>ขนาดของผลิตภัณฑ์ที่ใช้ร่วมกัน

เอนทิตี้ **ขนาดผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้ขนาดที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน ตารางต่อไปนี้แสดงการแม็ป

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>ลักษณะของผลิตภัณฑ์ที่ใช้ร่วมกัน

เอนทิตี้ **ลักษณะผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้ลักษณะที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน ตารางต่อไปนี้แสดงการแม็ป

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>การตั้งค่าคอนฟิกของผลิตภัณฑ์ที่ใช้ร่วมกัน

เอนทิตี้ **การตั้งค่าคอนฟิกของผลิตภัณฑ์ที่ใช้ร่วมกัน** บ่งชี้การตั้งค่าคอนฟิกที่ผลิตภัณฑ์หลักที่ระบุสามารถมีได้ แนวคิดนี้ถูกย้ายไปที่ Common Data Service เพื่อให้ข้อมูลสอดคล้องกัน ตารางต่อไปนี้แสดงการแม็ป

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>บาร์โค้ดของตัวระบุหมายเลขผลิตภัณฑ์

บาร์โคดของผลิตภัณฑ์ถูกใช้เพื่อระบุผลิตภัณฑ์โดยไม่ซ้ำ การแม็ปต่อไปนี้ถูกใช้เพื่อสร้างบาร์โคดของผลิตภัณฑ์ที่พร้อมใช้งานใน Common Data Service

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARCODE | \> | msdyn\_name
BARCODE | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>การตั้งค่าใบสั่งเริ่มต้นและการตั้งค่าใบสั่งเริ่มต้นเฉพาะผลิตภัณฑ์

การตั้งค่าใบสั่งเริ่มต้นกำหนดไซต์และคลังสินค้าที่สินค้าจะเป็นต้นทางหรือจัดเก็บ ปริมาณต่ำสุด สูงสุด หลายรายการ และมาตรฐานที่จะใช้สำหรับการค้าหรือการจัดการสินค้าคงคลัง ระยะเวลารอคอยสินค้า แฟล็กหยุด และวิธีการสัญญาว่าจะออกใบสั่ง ข้อมูลเหล่านี้จะมีอยู่ใน CDS โดยใช้การตั้งค่าใบสั่งเริ่มต้นและเอนทิตี้การตั้งค่าใบสั่งเริ่มต้นเฉพาะผลิตภัณฑ์ คุณสามารถอ่านข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันบน [หน้าการตั้งค่าใบสั่งเริ่มต้น](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings)

### <a name="default-order-settings"></a>การตั้งค่าใบสั่งเริ่มต้น

การแม็ปต่อไปนี้ถูกใช้เพื่อให้การตั้งค่าใบสั่งเริ่มต้นพร้อมใช้งานใน Common Data Service

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>การตั้งค่าใบสั่งเริ่มต้นโดยเฉพาะของผลิตภัณฑ์

การแม็ปต่อไปนี้ถูกใช้เพื่อให้การตั้งค่าใบสั่งเริ่มต้นที่ระบุของผลิตภัณฑ์พร้อมใช้งานใน Common Data Service

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>หน่วยวัดและการแปลงหน่วยวัด

หน่วยวัดและการแปลงที่เกี่ยวข้องจะพร้อมใช้งานใน Common Data Service ตามแบบจำลองข้อมูลต่อไปนี้ที่แสดงในแผนภาพ

![แบบจำลองข้อมูลสำหรับผลิตภัณฑ์](media/dual-write-product-3.PNG)

แนวคิดหน่วยวัดถูกรวมกันระหว่างแอป Finance and Operations และแอปอื่นๆของ Dynamics 365 สำหรับประเภทของหน่วยแต่ละประเภทในแอพป Finance and Operations กลุ่มหน่วยจะถูกสร้างขึ้นในแอป Dynamics 365 ซึ่งประกอบด้วยหน่วยที่อยู่ในประเภทของหน่วย นอกจากนี้ยังมีการสร้างหน่วยพื้นฐานเริ่มต้นสำหรับทุกกลุ่มหน่วยด้วย 

### <a name="unit-of-measure"></a>หน่วยวัด

การแม็ปต่อไปนี้ถูกใช้เพื่อให้หน่วยวัดในแอป Finance and Operations พร้อมใช้งานใน Common Data Service

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | name
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>การแปลงหน่วยวัด

การแม็ปต่อไปนี้ถูกใช้เพื่อให้การแปลงหน่วยวัดในแอป Finance and Operations พร้อมใช้งานใน Common Data Service

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol

### <a name="product-specific-unit-of-measure-conversions"></a>การแปลงหน่วยวัดเฉพาะของผลิตภัณฑ์

การแม็ปต่อไปนี้ถูกใช้เพื่อให้การแปลงหน่วยวัดที่ระบุของผลิตภัณฑ์ในแอป Finance and Operations พร้อมใช้งานใน Common Data Service

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>นโยบายผลิตภัณฑ์ คือ มิติ การติดตาม และกลุ่มการจัดเก็บ

นโยบายผลิตภัณฑ์เป็นชุดของนโยบายที่ใช้สำหรับการกำหนดผลิตภัณฑ์และลักษณะของสินค้าในสินค้าคงคลัง กลุ่มมิติของผลิตภัณฑ์ กลุ่มมิติการติดตามของผลิตภัณฑ์ และกลุ่มมิติการจัดเก็บสามารถพบได้เป็นนโยบายผลิตภัณฑ์ 

### <a name="product-dimension-group"></a>กลุ่มมิติของผลิตภัณฑ์

กลุ่มมิติของผลิตภัณฑ์ที่กำหนดว่ามิติของผลิตภัณฑ์ใดที่กำหนดผลิตภัณฑ์ กลุ่มมิติของผลิตภัณฑ์ที่เป็นไปได้สี่กลุ่ม คือ ขนาด สี ลักษณะ และการตั้งค่าคอนฟิก กลุ่มมิติของผลิตภัณฑ์พร้อมใช้งานใน Common Data Service โดยใช้การแม็ปดังต่อไปนี้ 

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>กลุ่มมิติของการติดตามผลิตภัณฑ์

กลุ่มมิติของการติดตามผลิตภัณฑ์แสดงวิธีการที่ใช้ในการติดตามผลิตภัณฑ์ในสินค้าคงคลัง เหล่านี้พร้อมใช้งานใน Common Data Service โดยใช้การแม็ปดังต่อไปนี้ 

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>กลุ่มมิติของการจัดเก็บผลิตภัณฑ์

กลุ่มมิติของการจัดเก็บผลิตภัณฑ์แสดงวิธีการที่ใช้กำหนดการจัดวางผลิตภัณฑ์ในคลังสินค้า เหล่านี้พร้อมใช้งานใน Common Data Service โดยใช้การแม็ปดังต่อไปนี้ 

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation

