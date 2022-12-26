---
title: แพคเกจการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทางที่แยกต่างหาก
description: แพคเกจการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทางไม่ใช่แพคเกจเดียวอีกต่อไป แต่ถูกแยกออกเป็นแพคเกจที่เล็กลง บทความนี้อธิบายโซลูชันและแมปกับแต่ละแพคเกจมี และการขึ้นต่อกันกับแพคเกจอื่นๆ
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 7f2a9b9e52b80c0feae0ac0dcb1ddf0a5c0cd27c
ms.sourcegitcommit: 8aba7d2f45ef03a14f33f4b430ce92a11c876e2e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/16/2022
ms.locfileid: "9884128"
---
# <a name="separated-dual-write-application-orchestration-package"></a>แพคเกจการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทางที่แยกต่างหาก

[!include [banner](../../includes/banner.md)]



แพคเกจการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทางเป็นแพคเกจเดียวที่มีโซลูชันต่อไปนี้:

- Dynamics 365 Notes
- Dynamics 365 Common Anchor สำหรับการเงินและการดำเนินงาน
- แผนที่เอนทิตี้การรวมแบบสองทิศทางสำหรับ Dynamics 365 การเงินและการดำเนินงาน
- แอปการจัดการสินทรัพย์ของ Dynamics 365
- การจัดการสินทรัพย์ของ Dynamics 365
- HCM ทั่วไป
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 การเงินและการดำเนินงาน Common
- Dynamics 365 Company
- อัตราแลกเปลี่ยนสกุลเงิน
- Field Service Common

เนื่องจากเป็นแพคเกจเดียว แพคเกจนี้จะสร้างสถานการณ์ "ทั้งหมดหรือไม่มี" ให้กับลูกค้า อย่างไรก็ตาม ขณะนี้ Microsoft แยกผลิตภัณฑ์ออกเป็นแพคเกจที่เล็กลง ดังนั้น ลูกค้าจึงสามารถเลือกเฉพาะแพคเกจของโซลูชันที่ต้องการ ตัวอย่างเช่น ถ้าคุณเป็นลูกค้า Microsoft Dynamics 365 Supply Chain Management และไม่ต้องการรวมเข้ากับ Dynamics 365 Human Resources, Notes และการจัดการสินทรัพย์ คุณสามารถแยกโซลูชันเหล่านั้นออกจากโซลูชันที่ติดตั้ง เนื่องจากชื่อโซลูชัน ผู้เผยแพร่ และรุ่นแผนผังที่อยู่ภายใต้ยังคงเหมือนเดิม การเปลี่ยนแปลงนี้จึงไม่ใช่การแบ่ง การติดตั้งที่มีอยู่จะถูกอัปเกรด

![แพคเกจที่แยกต่างหาก](media/separated-package-1.png)

บทความนี้อธิบายโซลูชันและแมปกับแต่ละแพคเกจมี และการขึ้นต่อกันกับแพคเกจอื่นๆ

## <a name="dual-write-application-core"></a>แอปพลิเคชันการรวมแบบสองทิศทางหลัก

แพคเกจหลักของแอปพลิเคชันการรวมแบบสองทิศทางจะช่วยให้ผู้ใช้สามารถติดตั้งและตั้งค่าคอนฟิกการรวมแบบสองทิศทางโดยไม่มีแอปการมีส่วนร่วมของลูกค้าใดๆ ซึ่งประกอบด้วยห้าโซลูชันต่อไปนี้

| ชื่อเฉพาะ                           | ชื่อที่แสดง                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 การเงินและการดำเนินงาน Common |
| CurrencyExchangeRates                 | อัตราแลกเปลี่ยนสกุลเงิน                    |
| msdyn_DualWriteAppCoreMaps            | แผนผังเอนทิตีหลักของแอปพลิเคชันการรวมแบบสองทิศทาง   |
| msdyn_DualWriteAppCoreAnchor          | จุดยึดหลักของแอปพลิเคชันการรวมแบบสองทิศทาง        |

แผนผังต่อไปนี้จะพร้อมใช้งานในแพคเกจนี้

| แอปการเงินและการดำเนินงาน     | แอปการมีส่วนร่วมของลูกค้า                    |
|---------------------------------|---------------------------------------------|
| หน่วยปฏิบัติงาน                  | msdyn_internalorganizations                 |
| ลำดับชั้นขององค์กร          | msdyn_internalorganizationhierarchies       |
| นิติบุคคล                  | msdyn_internalorganizations                 |
| นิติบุคคล                  | cdm_companies                               |
| วัตถุประสงค์ลำดับชั้นขององค์กร | msdyn_internalorganizationhierarchypurposes |
| คู่สกุลเงินของอัตราแลกเปลี่ยน     | msdyn_currencyexchangeratepairs             |
| ส่วนเพิ่มของชื่อ                    | msdyn_nameaffixes                           |
| ชนิดอัตราแลกเปลี่ยน              | msdyn_exchangeratetypes                     |
| อัตราแลกเปลี่ยน CDS              | msdyn_currencyexchangerates                 |
| ชนิดลำดับชั้นขององค์กร     | msdyn_internalorganizationhierarchytypes    |
| สกุลเงิน                      | transactioncurrencies                       |
| เอนทิตี้คู่มือความเป็นจริงผสม     | msmrw_guides                                |

**ข้อมูลการขึ้นต่อกัน**

แพคเกจหลักของแอปพลิเคชันการรวมแบบสองทิศทางไม่มีการขึ้นต่อกันกับแพคเกจอื่น

## <a name="dual-write-human-resources"></a>Human Resources ของการรวมแบบสองทิศทาง

แพคเกจ Human Resources ของการรวมแบบสองทิศทางมีโซลูชันและแผนผังที่ต้องใช้ในการซิงค์ข้อมูล Human Resources ซึ่งประกอบด้วยสามโซลูชันต่อไปนี้

| ชื่อเฉพาะ                | ชื่อที่แสดง                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM ทั่วไป                               |
| msdyn_Dynamics365HCMMaps   | แม็บเอนทิตี Dynamics 365 Human Resources |
| msdyn_Dynamics365HCMAnchor | จุดยึด Dynamics 365 Human Resources      |

แผนผังต่อไปนี้จะพร้อมใช้งานในแพคเกจนี้

| แอปการเงินและการดำเนินงาน | แอปการมีส่วนร่วมของลูกค้า         |
|-----------------------------|----------------------------------|
| เชื้อชาติ              | cdm_ethnicorigins                |
| ฟังก์ชันงานค่าตอบแทน   | cdm_jobfunctions                 |
| ตำแหน่งงาน V2                | cdm_jobpositions                 |
| งาน                        | cdm_jobs                         |
| ชนิดของงานค่าตอบแทน       | cdm_jobtypes                     |
| รหัสภาษา              | cdm_languages                    |
| ชนิดของตำแหน่ง               | cdm_positiontypes                |
| การมอบหมายผู้ปฏิบัติงานให้กับตำแหน่งงาน | cdm_positionworkerassignmentmaps |
| สถานะทหารผ่านศึก              | cdm_veteranstatuses              |
| ผู้ปฏิบัติงาน                      | cdm_workers                      |
| การจ้างงานต่อบริษัท      | cdm_employments                  |

**ข้อมูลการขึ้นต่อกัน**

แพคเกจ Human Resources ของการรวมแบบสองทิศทางจะขึ้นอยู่กับแพคเกจของแอปพลิเคชันการรวมแบบสองทิศทางหลัก ดังนั้น คุณจึงควรติดตั้งแพคเกจแอปพลิเคชันการรวมแบบสองทิศทางหลักก่อนที่จะติดตั้งแพคเกจ Human Resources ของการรวมแบบสองทิศทาง

## <a name="dual-write-supply-chain"></a>Supply Chain การรวมแบบสองทิศทาง

แพคเกจ Supply Chain ของการรวมแบบสองทิศทางมีโซลูชันและแผนผังที่ต้องใช้ในการซิงค์ข้อมูล Supply Chain Management ซึ่งประกอบด้วยสามโซลูชันต่อไปนี้

| ชื่อเฉพาะ                                | ชื่อที่แสดง                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | แมปเอนทิตี Dynamics 365 Supply Chain Management เพิ่มเติม |
| msdyn_Dynamics365SupplyChainExtendedAnchor | จุดยึด Dynamics 365 Supply Chain Management เพิ่มเติม      |

แผนผังต่อไปนี้จะพร้อมใช้งานในแพคเกจนี้

| แอปการเงินและการดำเนินงาน                 | แอปการมีส่วนร่วมของลูกค้า                      |
|---------------------------------------------|-----------------------------------------------|
| หน่วย                                       | uoms                                          |
| ส่วนหัวของใบสั่งขาย CDS                     | salesorders                                   |
| รายการในใบสั่งขาย CDS                       | salesorderdetails                             |
| ส่วนหัวของใบเสนอราคาขาย CDS                  | ใบเสนอราคา                                        |
| รายการในใบเสนอราคาขาย CDS                   | quotedetails                                  |
| ผลิตภัณฑ์เฉพาะที่นำออกใช้ CDS              | ผลิตภัณฑ์                                      |
| โซนคลังสินค้า                             | msdyn_warehousezones                          |
| กลุ่มโซนคลังสินค้า                       | msdyn_warehousezonegroups                     |
| รายการงานของคลังสินค้า                        | msdyn_warehouseworklines                      |
| ส่วนหัวของงานคลังสินค้า                      | msdyn_warehouseworkheaders                    |
| คลังสินค้า                                  | msdyn_warehouses                              |
| ที่เก็บสินค้าคงคลัง                             | msdyn_warehouseaisles                         |
| การแปลงหน่วย                            | msdyn_unitofmeasureconversions                |
| เงื่อนไขการจัดส่ง                           | msdyn_termsofdeliveries                       |
| วิธีการจัดส่ง                           | msdyn_shipvias                                |
| ลักษณะของผลิตภัณฑ์หลัก                       | msdyn_sharedproductstyles                     |
| รายการในใบแจ้งหนี้การขาย V2                      | invoicedetails                                |
| ส่วนหัวของใบแจ้งหนี้การขาย V2                    | ใบแจ้งหนี้                                      |
| ขนาดของผลิตภัณฑ์หลัก                        | msdyn_sharedproductsizes                      |
| ผลิตภัณฑ์ที่นำออกใช้ V2                        | msdyn_sharedproductdetails                    |
| การตั้งค่าคอนฟิกผลิตภัณฑ์หลัก               | msdyn_sharedproductconfigurations             |
| สีของผลิตภัณฑ์หลัก                       | msdyn_sharedproductcolors                     |
| รหัสจุดเริ่มต้นของใบสั่งขาย                    | msdyn_salesorderorigins                       |
| ส่วนหัวของใบรับสินค้า                      | msdyn_purchaseorderreceipts                   |
| รายการใบรับสินค้า                        | msdyn_purchaseorderreceiptproducts            |
| ส่วนหัวของใบสั่งซื้อ V2                   | msdyn_purchaseorders                          |
| เอนทิตี้การลบชั่วคราวสำหรับรายการใบสั่งซื้อของ CDS | msdyn_purchaseorderproducts                   |
| เอนทิตี้รายการในใบสั่งซื้อ CDS              | msdyn_purchaseorderproducts                   |
| กลุ่มมิติการติดตาม                   | msdyn_producttrackingdimensiongroups          |
| ลักษณะ                                      | msdyn_productstyles                           |
| กลุ่มมิติการจัดเก็บ                    | msdyn_productstoragedimensiongroups           |
| การแปลงหน่วยเฉพาะผลิตภัณฑ์           | msdyn_productspecificunitofmeasureconversions |
| การตั้งค่าใบสั่งเริ่มต้นของผลิตภัณฑ์ V2           | msdyn_productspecificdefaultordersettings     |
| ขนาด                                       | msdyn_productsizes                            |
| กลุ่มมิติของผลิตภัณฑ์                    | msdyn_productdimensiongroups                  |
| การตั้งค่าใบสั่งเริ่มต้น                      | msdyn_productdefaultordersettings             |
| โครงแบบ                              | msdyn_productconfigurations                   |
| ผลิตภัณฑ์ทั้งหมด                                | msdyn_globalproducts                          |
| สี                                      | msdyn_productcolors                           |
| บทบาทการจัดประเภทตามลำดับชั้นของผลิตภัณฑ์            | msdyn_productcategoryhierarchyroles           |
| การจัดประเภทตามลำดับชั้นของผลิตภัณฑ์                | msdyn_productcategoryhierarchies              |
| การกำหนดประเภทผลิตภัณฑ์                | msdyn_productcategoryassignments              |
| ประเภทผลิตภัณฑ์                          | msdyn_productcategories                       |
| ที่ตั้งคลังสินค้า                         | msdyn_inventorylocations                      |
| สินค้าคงคลังคงเหลือ CDS                            | msdyn_inventoryonhandentries                  |
| ประเภทผลิตภัณฑ์                          | msdyn_productcategories                       |
| สินค้าคงคลังคงเหลือ CDS                            | msdyn_inventoryonhandrequests                 |
| บาร์โค้ดที่ระบุหมายเลขผลิตภัณฑ์           | msdyn_productbarcodes                         |
| บัตรสมาชิก                                | msdyn_loyaltycards                            |
| คะแนนรางวัลสำหรับสมาชิก                       | msdyn_loyaltyrewardpoints                     |
| กลุ่มลูกค้าที่มีการกำหนดราคา                       | msdyn_pricecustomergroups                     |
| ไซต์                                       | msdyn_operationalsites                        |
| รายการในใบเสนอราคาขาย CDS                   | quotedetails                                  |
| รายการในใบสั่งขาย CDS                       | salesorderdetails                             |

**ข้อมูลการขึ้นต่อกัน**

แพคเกจ Supply Chain ของการรวมแบบสองทิศทางขึ้นอยู่กับสามแพคเกจต่อไปนี้ ดังนั้น คุณจึงควรติดตั้งแพคเกจเหล่านี้ก่อนที่คุณจะติดตั้งแพคเกจ Supply Chain ของการรวมแบบสองทิศทาง

- แพคเกจแอปพลิเคชันการรวมแบบสองทิศทางหลัก
- แพคเกจ Finance ของการรวมแบบสองทิศทาง
- แพคเกจ Human Resources ของการรวมแบบสองทิศทาง
- Dynamics 365 HR Common Tables

## <a name="dual-write-finance"></a>Finance ของการรวมแบบสองทิศทาง

แพคเกจ Finance ของการรวมแบบสองทิศทางมีโซลูชันและแผนผังที่ต้องใช้ในการซิงค์ข้อมูล Dynamics 365 Finance ซึ่งประกอบด้วยสี่โซลูชันต่อไปนี้

| ชื่อเฉพาะ                            | ชื่อที่แสดง                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | แผนผังเอนทิตี้ Dynamics 365 Finance Extended |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | จุดยึด Dynamics 365 Finance Extended      |

แผนผังต่อไปนี้จะพร้อมใช้งานในแพคเกจนี้

| แอปการเงินและการดำเนินงาน             | แอปการมีส่วนร่วมของลูกค้า        |
|-----------------------------------------|---------------------------------|
| กลุ่มภาษีหัก ณ ที่จ่าย                  | msdyn_withholdingtaxgroups      |
| CDS ผู้ติดต่อ V2 (ลูกค้า)              | ผู้ติดต่อ                        |
| CDS ผู้ติดต่อ V2 (ผู้จัดจำหน่าย)                | ผู้ติดต่อ                        |
| ลูกค้า V3                            | ผู้ติดต่อ                        |
| รหัสภาษีหัก ณ ที่จ่าย                   | msdyn_withholdingtaxcodes       |
| ผู้จัดจำหน่าย V2                              | msdyn_vendors                   |
| วิธีการชำระเงินของผู้จัดจำหน่าย                   | msdyn_vendorpaymentmethods      |
| กลุ่มผู้จัดจำหน่าย                           | msdyn_vendorgroups              |
| ผังบัญชี                       | msdyn_chartofaccountses         |
| กลุ่มการลงรายการบัญชีแยกประเภทของภาษีขาย V2      | msdyn_taxpostinggroups          |
| กลุ่มภาษีขายตามประเภทสินค้า                    | msdyn_taxitemgroups             |
| กลุ่มภาษีขาย                        | msdyn_taxgroups                 |
| เอนทิตี้รหัสยกเว้นภาษีขายสำหรับ CDS        | msdyn_taxexemptcodes            |
| กลุ่มลูกค้า                         | msdyn_customergroups            |
| วิธีการชำระเงินของลูกค้า                 | msdyn_customerpaymentmethods    |
| มิติทางการเงิน                    | msdyn_dimensionattributes       |
| หน่วยงานจัดเก็บภาษีขาย                   | msdyn_taxauthorities            |
| รูปแบบมิติทางการเงิน              | msdyn_financialdimensionformats |
| รอบระยะเวลาปฏิทินทางการเงิน                  | msdyn_fiscalcalendarperiods     |
| เอนทิตี้การรวมปฏิทินทางการเงิน      | msdyn_fiscalcalendars           |
| เอนทิตี้การรวมปีปฏิทินทางการเงิน | msdyn_fiscalcalendaryears       |
| เงื่อนไขการชำระเงิน                        | msdyn_paymentterms              |
| กำหนดการชำระเงิน                        | msdyn_paymentschedules          |
| รายการกำหนดการชำระเงิน                  | msdyn_paymentschedulelines      |
| CDS จำนวนวันการชำระเงิน                        | msdyn_paymentdays               |
| รายการแสดงวันที่ในการชำระเงินของ CDS V2                | msdyn_paymentdaylines           |
| บัญชีหลัก                            | msdyn_mainaccounts              |
| ประเภทบัญชีหลัก                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| ลูกค้า V3                            | บัญชี                        |

**ข้อมูลการขึ้นต่อกัน**

แพคเกจ Finance ของการรวมแบบสองทิศทางจะขึ้นอยู่กับแพคเกจของแอปพลิเคชันการรวมแบบสองทิศทางหลัก ดังนั้น คุณจึงควรติดตั้งแพคเกจแอปพลิเคชันการรวมแบบสองทิศทางหลักก่อนที่จะติดตั้งแพคเกจ Finance ของการรวมแบบสองทิศทาง

## <a name="dual-write-notes"></a>Notes ของการรวมแบบสองทิศทาง

แพคเกจ Notes ของการรวมแบบสองทิศทางมีโซลูชันและแผนผังที่ต้องใช้ในการซิงค์ข้อมูลบันทึกหรือคำอธิบายประกอบ ซึ่งประกอบด้วยสี่โซลูชันต่อไปนี้

| ชื่อเฉพาะ                  | ชื่อที่แสดง                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 Notes เพิ่มเติม    |
| msdyn_Dynamics365NotesMaps   | แมปเอนทิตี Dynamics 365 Notes |
| msdyn_Dynamics365NotesAnchor | จุดยึดบันทึก Dynamics 365      |

แผนผังต่อไปนี้จะพร้อมใช้งานในแพคเกจนี้

| การเงินและการดำเนินงาน                     | Customer Engagement |
|--------------------------------------------|---------------------|
| เอกสารแนบส่วนหัวของใบสั่งขาย    | คำอธิบายประกอบ         |
| เอกสารแนบของลูกค้า                       | คำอธิบายประกอบ         |
| สิ่งที่แนบของเอกสารสำหรับผู้จัดจำหน่าย                | คำอธิบายประกอบ         |
| เอกสารแนบส่วนหัวของใบสั่งซื้อ | คำอธิบายประกอบ         |

**ข้อมูลการขึ้นต่อกัน**

แพคเกจ Notes ของการรวมแบบสองทิศทางขึ้นอยู่กับสองแพคเกจต่อไปนี้ ดังนั้น คุณจึงควรติดตั้งแพคเกจเหล่านี้ก่อนที่คุณจะติดตั้งแพคเกจ Notes ของการรวมแบบสองทิศทาง

- แพคเกจแอปพลิเคชันการรวมแบบสองทิศทางหลัก
- แพคเกจ Finance ของการรวมแบบสองทิศทาง

## <a name="dual-write-asset-management"></a>การจัดการสินทรัพย์ของการรวมแบบสองทิศทาง

แพคเกจการจัดการสินทรัพย์ของการรวมแบบสองทิศทางมีโซลูชันและแผนผังที่ต้องใช้ในการซิงค์ข้อมูลสินทรัพย์จาก Supply Chain Management หรือ Dynamics 365 Field Service ซึ่งประกอบด้วยสี่โซลูชันต่อไปนี้

| ชื่อเฉพาะ                          | ชื่อที่แสดง                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | การจัดการสินทรัพย์ของ Dynamics 365             |
| Dynamics365AssetManagementApp        | แอป Dynamics 365 การจัดการสินทรัพย์          |
| msdyn_DualWriteAssetManagementMaps   | แมปเอนทิตี Dynamics 365 การจัดการสินทรัพย์ |
| msdyn_DualWriteAssetManagementAnchor | จุดยึด Dynamics 365 การจัดการสินทรัพย์      |

แผนผังต่อไปนี้จะพร้อมใช้งานในแพคเกจนี้

| แอปการเงินและการดำเนินงาน                           | แอปการมีส่วนร่วมของลูกค้า                |
|-------------------------------------------------------|-----------------------------------------|
| การรับประกันของการจัดการสินทรัพย์                             | msdyn_warranties                        |
| แบบจำลองการจัดการสินทรัพย์                               | msdyn_models                            |
| ผู้ผลิตของการจัดการสินทรัพย์                        | msdyn_manufacturers                     |
| ชนิดของตำแหน่งที่ทำงานในการจัดการสินทรัพย์            | msdyn_functionallocationtypes           |
| ตำแหน่งที่ทำงานในการจัดการสินทรัพย์                 | msdyn_functionallocations               |
| สถานะของวงจรการใช้ของตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn_functionallocationlifecyclestates |
| แบบจำลองวงจรการใช้งานของตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn_functionallocationlifecyclemodels |
| สินทรัพย์ในการจัดการสินทรัพย์                               | msdyn_customerassets                    |
| ชนิดสินทรัพย์ในการจัดการสินทรัพย์                          | msdyn_customerassetcategories           |
| สถานะของวงจรการใช้ของสินทรัพย์ในการจัดการสินทรัพย์               | msdyn_assetlifecyclestates              |
| แบบจำลองวงจรการใช้งานของสินทรัพย์ในการจัดการสินทรัพย์               | msdyn_assetlifecyclemodels              |

**ข้อมูลการขึ้นต่อกัน**

แพคเกจการจัดการสินทรัพย์ของการรวมแบบสองทิศทางจะขึ้นอยู่กับแพคเกจของแอปพลิเคชันการรวมแบบสองทิศทางหลัก ดังนั้น คุณจึงควรติดตั้งแพคเกจแอปพลิเคชันการรวมแบบสองทิศทางหลักก่อนที่จะติดตั้งแพคเกจการจัดการสินทรัพย์ของการรวมแบบสองทิศทาง

## <a name="packages-required-for-project-operations"></a>แพคเกจที่ Project Operations ต้องใช้
Project Operations จะขึ้นอยู่กับแพคเกจต่อไปนี้ ดังนั้น คุณจึงควรติดตั้งแพคเกจเหล่านี้ก่อนที่คุณจะติดตั้ง Project Operations

- แพคเกจแอปพลิเคชันการรวมแบบสองทิศทางหลัก
- แพคเกจ Finance ของการรวมแบบสองทิศทาง
- แพคเกจ Supply Chain การรวมแบบสองทิศทาง
- แพคเกจการจัดการสินทรัพย์ของการรวมแบบสองทิศทาง
- แพคเกจ Human Resources ของการรวมแบบสองทิศทาง

## <a name="dual-write-party-and-global-address-book-solutions"></a>ฝ่ายการรวมแบบสองทิศทางและโซลูชันสมุดที่อยู่สากล

แพคเกจฝ่ายการรวมแบบสองทิศทางและสมุดที่อยู่สากลประกอบด้วยโซลูชันและแผนผังต่อไปนี้ซึ่งจำเป็นต่อการซิงค์ข้อมูลฝ่ายและสมุดที่อยู่สากล 

| ชื่อเฉพาะ                       | ชื่อที่แสดง                            |
|-----------------------------------|-----------------------------------------|
| ฝ่าย                             | ฝ่าย                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB Extended               |
| Dynamics365GABDualWriteEntityMaps | แผนผังเอนทิตี้การรวมแบบสองทิศทาง Dynamics 365 GAB |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAB และฝ่าย              |

แผนผังต่อไปนี้จะพร้อมใช้งานในแพคเกจนี้

| แอปการเงินและการดำเนินงาน | แอปการมีส่วนร่วมของลูกค้า | 
|-----------------------------|--------------------------|
| ฝ่าย CDS | msdyn_parties | 
| สถานที่ของที่อยู่ทางไปรษณีย์ของ CDS | msdyn_postaladdresscollections | 
| ประวัติที่อยู่ทางไปรษณีย์ของ CDS V2 | msdyn_postaladdresses | 
| สถานที่ของที่อยู่ทางไปรษณีย์ของฝ่าย CDS | msdyn_partypostaladdresses | 
| ผู้ติดต่อของฝ่าย V3 | msdyn_partyelectronicaddresses | 
| ลูกค้า V3 | บัญชี | 
| ลูกค้า V3 | ผู้ติดต่อ | 
| ผู้จัดจำหน่าย V2 | msdyn_vendors | 
| ตำแหน่งของผู้ติดต่อ | msdyn_salescontactpersontitles | 
| คำลงท้าย | msdyn_complimentaryclosings | 
| คำขึ้นต้น | msdyn_salutations | 
| บทบาทในการตัดสินใจ | msdyn_decisionmakingroles | 
| ฟังก์ชันงานในการจ้างงาน | msdyn_employmentjobfunctions | 
| ระดับของสมาชิก | msdyn_loyaltylevels | 
| ชนิดลักษณะส่วนบุคคล | msdyn_personalcharactertypes | 
| ผู้ติดต่อ V2 | msdyn_contactforparties | 
| ส่วนหัวของใบเสนอราคาขาย CDS | ใบเสนอราคา | 
| ส่วนหัวของใบสั่งขาย CDS | salesorders | 
| ส่วนหัวของใบแจ้งหนี้การขาย V2 | ใบแจ้งหนี้ | 
| บทบาทที่อยู่ CDS | msdyn_addressroles |

**ข้อมูลการขึ้นต่อกัน**

ฝ่ายการรวมแบบสองทิศทางและโซลูชันสมุดที่อยู่สากลขึ้นอยู่กับสามแพคเกจต่อไปนี้ ดังนั้น คุณจึงควรติดตั้งแพคเกจเหล่านี้ก่อนที่คุณจะติดตั้งแพคเกจฝ่ายการรวมแบบสองทิศทางและโซลูชันสมุดที่อยู่สากล

- แพคเกจแอปพลิเคชันการรวมแบบสองทิศทางหลัก
- แพคเกจ Finance ของการรวมแบบสองทิศทาง
- แพคเกจ Supply Chain การรวมแบบสองทิศทาง

