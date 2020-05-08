---
title: ห่วงลำดับการอ้างอิงของเอนทิตี้ (ลำดับการซิงโครไนส์)
description: หัวข้อนี้ระบุลำดับของการซิงโครไนส์ที่คุณต้องปฏิบัติตามเพื่อสร้างข้อมูลเริ่มต้น
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275498"
---
# <a name="entity-dependency-chain-synchronization-order"></a>ห่วงลำดับการอ้างอิงของเอนทิตี้ (ลำดับการซิงโครไนส์)

[!include [banner](../../includes/banner.md)]

หัวข้อนี้จะระบุลำดับของการซิงโครไนส์ที่คุณต้องปฏิบัติตามเพื่อสร้างข้อมูลเริ่มต้น ถ้าคุณไม่ได้ใช้การที่ขึ้นต่อกันกับเอนทิตี้ที่ระบุโดยคุณลักษณะ **การซิงค์เริ่มต้น** ถ้าคุณไม่ได้ใช้ **การซิงค์เริ่มต้น** คุณต้องรันแม็ปเอนทิตี้แต่ละทีละรายการ

## <a name="dynamics-365-supply-chain-management-entities"></a>เอนทิตี้ Dynamics 365 Supply Chain Management

เอนทิตี้ต่อไปนี้สำหรับ Supply Chain Management จะแสดงรายการตามลำดับที่คุณควรเปิดใช้งาน

| ชื่อการแม็ปในหน้าการรวมแบบสองทิศทาง | ชื่อข้อมูลเมตาของเอนทิตี้ใน Supply Chain Management | ชื่อข้อมูลเมตาของเอนทิตี้ใน Common Data Service | หมายเหตุ |
|---|---|---|---|
| หน่วย ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| การแปลงหน่วย ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| ผลิตภัณฑ์ทั้งหมด ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| กลุ่มมิติของผลิตภัณฑ์ ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| กลุ่มมิติการจัดเก็บ ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| กลุ่มมิติการติดตาม ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| สี ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| ขนาด ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| ลักษณะ ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| การจัดโครงแบบ ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| ผลิตภัณฑ์ที่นำออกใช้ V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| ผลิตภัณฑ์เฉพาะที่นำออกใช้ของ Common Data Service ... products                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | product / ผลิตภัณฑ์                                      | |
| บาร์โค้ดที่ระบุหมายเลขผลิตภัณฑ์ ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| การตั้งค่าใบสั่งเริ่มต้น ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| การตั้งค่าใบสั่งเริ่มต้นของผลิตภัณฑ์ V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| การแปลงหน่วยเฉพาะผลิตภัณฑ์ ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| ไซต์ ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| คลังสินค้า ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | ดู [หมายเหตุ 1](#scm-notes) |
| สีของผลิตภัณฑ์หลัก ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| ขนาดของผลิตภัณฑ์หลัก ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| ลักษณะของผลิตภัณฑ์หลัก ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| การจัดโครงแบบของผลิตภัณฑ์หลัก ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| ประเภทผลิตภัณฑ์ ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | ดู [หมายเหตุ 2](#scm-notes) |
| การกำหนดประเภทของผลิตภัณฑ์ ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| การจัดประเภทตามลำดับชั้นของผลิตภัณฑ์ ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| บทบาทการจัดประเภทตามลำดับชั้นของผลิตภัณฑ์ ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| ที่เก็บสินค้าคงคลัง ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| โซนคลังสินค้า ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| กลุ่มโซนคลังสินค้า ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| สถานที่เก็บในคลังสินค้า ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | ดู [หมายเหตุ 3](#scm-notes) |
| ส่วนหัวงานของคลังสินค้า ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| บรรทัดงานของคลังสินค้า... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | ดู [หมายเหตุ 4](#scm-notes) |
| วิธีการจัดส่ง ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| เงื่อนไขในการจัดส่ง ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| รหัสจุดเริ่มต้นของใบสั่งขาย ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| ส่วนหัวของใบสั่งขาย Common Data Service ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| บรรทัดใบสั่งขาย Common Data Service ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| ส่วนหัวของใบเสนอราคาขาย Common Data Service ... quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | ใบเสนอราคา                                        | |
| บรรทัดใบเสนอราคาขาย Common Data Service ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| ส่วนหัวของใบแจ้งหนี้การขาย V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | invoice / ใบแจ้งหนี้                                      | |
| บรรทัดใบแจ้งหนี้การขาย V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>หมายเหตุเฉพาะการแม็ป

1. เนื่องจากเป็นการอ้างอิงตนเอง คุณอาจต้องเรียกใช้การซิงโครไนส์เริ่มแรกสองครั้ง
2. ตามค่าเริ่มต้น การซิงโครไนส์เริ่มแรกจะถูกปิดเนื่องจากความสัมพันธ์หลัก-รอง (แพลตฟอร์มไม่ดำเนินการจัดลำดับแบบ "สมาร์ท") ดังนั้น คุณต้องซิงค์ประเภทผลิตภัณฑ์ที่มีอยู่ด้วยตนเอง (ตัวอย่างเช่น ด้วยการอัพเดตข้อมูลคำอธิบายของประเภท) ในลำดับที่ถูกต้อง (ประเภทระดับรากก่อน แล้วตามด้วยระดับย่อยของระดับย่อย) ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> ประเภทและคุณลักษณะ \> การจัดประเภทตามลำดับชั้น** บนหน้า **การจัดประเภทตามลำดับชั้น** คุณสามารถเลือกแต่ละลำดับชั้นและดูประเภทของผลิตภัณฑ์ในลำดับชั้นนั้นได้
3. การแม็ปฟิลด์ค้นหา **ItemNumberInLocation** ที่วางเปล่าและโซนคลังสินค้าเพิ่มเติมรายการแรก รายการที่สอง และที่สามจะทำให้การซิงโครไนส์เริ่มแรกล้มเหลว ดังนั้น การแม็ปเหล่านี้จะถูกลบออกในตอนนี้
4. การแม็ปฟิลด์ **CaptureWeight** ที่ว่างเปล่าจะทำให้การซิงโครไนส์เริ่มแรกล้มเหลว ดังนั้น การแม็ปนี้จะถูกลบออกในตอนนี้

### <a name="setup-related-information"></a>ข้อมูลที่เกี่ยวข้องกับการตั้งค่า

+ เมื่อมีการสร้างเรกคอร์ดในเอนทิตี้ **ผลิตภัณฑ์** ในแอปที่เป็นแบบโมเดลใน Dynamics 365 เป็นครั้งแรก เรกคอร์ดเหล่านั้นจะมีสถานะเป็น **ฉบับร่าง** หากต้องการเปลี่ยนสถานะเป็น **ใช้งานอยู่** ไปที่ **การตั้งค่า \> การจัดการ \> การตั้งค่าระบบ \> การขาย** ในแอปที่เป็นแบบโมเดล และตั้งค่าตัวเลือก **สร้างผลิตภัณฑ์ในสถานะที่ใช้งานอยู่** เป็น **ใช่**
+ หากคุณสร้างเรกคอร์ดในเอนทิตี้ **ผลิตภัณฑ์** ในแอปที่เป็นแบบโมเดลใน Dynamics 365 หรือใน Common Data Service ก่อนที่คุณจะเปิดใช้งานการรวมแบบสองทิศทาง เรกคอร์ดเหล่านั้นจะได้รับการอัพเดตเฉพาะเมื่อคีย์ทั้งหมด รวมถึง **บริษัท** ตรงกับข้อมูลในแอป Finance and Operations
+ การซิงโครไนส์เอนทิตี้ **ผลิตภัณฑ์** เป็นแบบทิศทางเดียว จากแอป Finance and Operations ไปยัง Common Data Service หากมีการอัพเดตฟิลด์ที่ถูกแม็ปในเอนทิตี้ **ผลิตภัณฑ์** ในแอปที่เป็นแบบโมเดลใน Dynamics 365 การอัพเดตดังกล่าวจะมีการเขียนทับระหว่างการซิงโครไนส์ครั้งถัดไปจากแอป Finance and Operations

### <a name="known-issues"></a>ปัญหาที่ทราบ

- เกิดข้อผิดพลาดเมื่อมีการลบหน่วยในแอป Finance and Operations เมื่อมีการซิงค์หน่วยวัดจากแอป Finance and Operations ไปยัง Common Data Service จะมีการสร้างหน่วยแรกของคลาสเฉพาะเป็นหน่วยหลักและมีการป้องกันการลบ

    **การลดปัญหา:** ลบหน่วยใน Common Data Service ก่อน จากนั้นจะสามารถลบในแอป Finance and Operations ได้

- เกิดข้อผิดพลาดเมื่อมีการลบไซต์การดำเนินงานในแอป Common Data Service ข้อความแสดงข้อผิดพลาดระบุว่า "Infolog: คำเตือน: ไม่สามารถลบที่อยู่หลัก; คำเตือน: ไม่สามารถลบเรกคอร์ดเอนทิตี้ได้เนื่องจากการตรวจสอบความถูกต้องล้มเหลวสำหรับแหล่งข้อมูลต่อไปนี้: InventSiteLogisticsLocation (InventSiteLogisticsLocation)" ข้อผิดพลาดนี้เกิดจากปัญหาในเอนทิตี้ข้อมูลในแอป Finance and Operations

    **การลดปัญหา:** คุณสามารถลบไซต์ในแอป Finance and Operations ได้ จากนั้นไซต์จะถูกลบใน Common Data Service หากการแม็ปที่มีการรวมแบบสองทิศทางที่สอดคล้องกันทำงานอยู่

## <a name="dynamics-365-finance-entities"></a>เอนทิตี้ Dynamics 365 Finance

เอนทิตี้ต่อไปนี้สำหรับ Dynamics 365 Finance จะแสดงรายการตามลำดับที่คุณควรเปิดใช้งาน

| ชื่อการแม็ปในหน้าการรวมแบบสองทิศทาง | ชื่อข้อมูลเมตาของเอนทิตี้ใน Finance | ชื่อข้อมูลเมตาของเอนทิตี้ใน Common Data Service | หมายเหตุ |
|---|---|---|---|
| สกุลเงิน ... transactioncurrencies                                            | CurrencyEntity                              | สกุลเงิน                                   | |
| ชนิดอัตราแลกเปลี่ยน ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| คู่สกุลเงินของอัตราแลกเปลี่ยน ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| อัตราแลกเปลี่ยนของ Common Data Service ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | ดู [หมายเหตุ 1](#fin-notes) |
| เอนทิตี้การการรวมปฏิทินทางการเงิน ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| เอนทิตี้การการรวมปีปฏิทินทางการเงิน ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| รอบระยะเวลาปฏิทินทางการเงิน ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| ชนิดลำดับชั้นขององค์กร ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | ดู [หมายเหตุ 1](#fin-notes) |
| วัตถุประสงค์ของลำดับชั้นขององค์กร ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | ดู [หมายเหตุ 1](#fin-notes) |
| นิติบุคคล ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | ดู [หมายเหตุ 1](#fin-notes) |
| นิติบุคคล ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| หน่วยปฏิบัติงาน ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | ดู [หมายเหตุ 1](#fin-notes) |
| ลำดับชั้นขององค์กร - ที่เผยแพร่ ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | ดู [หมายเหตุ 1](#fin-notes) |
| ส่วนเพิ่มของชื่อ ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Common Data Service ของจำนวนวันการชำระเงิน ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Common Data Service ของรายการจำนวนวันการชำระเงิน V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| กำหนดการชำระเงิน ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| รายการกำหนดการชำระเงิน ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| เงื่อนไขในการชำระเงิน ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| วิธีการชำระเงินของลูกค้า ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| วิธีการชำระเงินของผู้จัดจำหน่าย ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| กลุ่มลูกค้า ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| กลุ่มผู้จัดจำหน่าย ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| กลุ่มภาษีขาย ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| กลุ่มภาษีขายตามประเภทสินค้า ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| กลุ่มการลงรายการบัญชีแยกประเภทของภาษีขาย V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Common Data Service ของเอนทิตี้รหัสยกเว้นภาษีขาย ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| หน่วยงานจัดเก็บภาษีขาย ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| รหัสภาษีขาย ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | ดู [หมายเหตุ 1](#fin-notes) |
| รูปแบบมิติทางการเงิน ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| มิติทางการเงิน ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| กลุ่มภาษีหัก ณ ที่จ่าย ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| รหัสภาษีหัก ณ ที่จ่าย ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| ผังบัญชี ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| บัญชีแยกประเภท ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | ดู [หมายเหตุ 1](#fin-notes) |
| ประเภทบัญชีหลัก ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| บัญชีหลัก ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| ลูกค้า V3 ... accounts                                                       | CustCustomerV3Entity                        | account / บัญชี                                    | ดู [หมายเหตุ 2](#fin-notes) |
| ลูกค้า V3 ... contacts                                                       | CustCustomerV3Entity                        | ผู้ติดต่อ                                    | ดู [หมายเหตุ 3](#fin-notes) |
| ผู้จัดจำหน่าย V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | ดู [หมายเหตุ 2](#fin-notes) |
| ผู้ติดต่อของ Common Data Service V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | ผู้ติดต่อ                                    | ดู [หมายเหตุ 4](#fin-notes) |
| ผู้ติดต่อของ Common Data Service V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | ผู้ติดต่อ                                    | ดู [หมายเหตุ 5](#fin-notes) |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>หมายเหตุเฉพาะการแม็ป

1. การซิงโครไนส์แบบทางเดียวเกิดขึ้นจากแอป Finance and Operations ไปยัง Common Data Service
2. เนื่องจากเป็นการอ้างอิงตนเอง คุณอาจต้องเรียกใช้การซิงโครไนส์เริ่มแรกมากกว่าหนึ่งครั้ง ตรวจสอบให้แน่ใจว่าได้เลือก **ลูกค้า** เป็นชนิดความสัมพันธ์เมื่อคุณสร้างบัญชีโดยใช้หน้า **บัญชี** ใน Common Data Service ถ้าคุณพบปัญหาเกี่ยวกับฟิลด์ **ผู้ติดต่อหลัก** ในระหว่างการซิงโครไนส์เริ่มแรก ให้ลบฟิลด์นั้นออกจากการแม็ป แล้วเรียกใช้การซิงโครไนส์เริ่มแรกอีกครั้ง หลังจากดำเนินการซิงโครไนส์เริ่มแรกเสร็จสมบูรณ์แล้ว ให้หยุดการแม็ป และเพิ่มฟิลด์ **ผู้ติดต่อหลัก** ในการซิงโครไนส์อีกครั้ง จากนั้นเริ่มต้นการแม็ป แต่ข้ามการซิงโครไนส์เริ่มแรก ค่าของฟิลด์ **ผู้ติดต่อหลัก** จะไม่รวมอยู่ในการซิงโครไนส์เริ่มแรกและคุณต้องย้ายค่านั้นด้วยตนเอง
3. ตรวจสอบให้แน่ใจว่าได้ตั้งค่าตัวเลือก **Sellable** เป็น **ใช่** ในหน้า **ผู้ติดต่อ** ใน Common Data Service เมื่อคุณพยายามสร้างลูกค้าเป็นชนิด **บุคคล**
4. การแม็ปนี้มีตัวกรองข้อมูลทั้งสองด้านเพื่อเชื่อมโยงผู้ติดต่อของลูกค้า เปิดรายละเอียดการแม็ป เลือกปุ่มตัวกรอง (สัญลักษณ์รูปกรวย) ที่อยู่ถัดจากชื่อเอนทิตี้ **Sales.Contact** และตรวจสอบให้แน่ใจว่าเงื่อนไขของไฟล์มี **msdyn_contactforvendor eq true and msdyn_sellable eq false**
5. การแม็ปนี้มีตัวกรองข้อมูลทั้งสองด้านเพื่อเชื่อมโยงผู้ติดต่อของผู้จัดจำหน่าย เปิดรายละเอียดการแม็ป เลือกปุ่มตัวกรอง (สัญลักษณ์รูปกรวย) ที่อยู่ถัดจากชื่อเอนทิตี้ **Sales.Contact** และตรวจสอบให้แน่ใจว่าเงื่อนไขของตัวกรองมี **msdyn_contactforvendor eq true and msdyn_sellable eq false** 

## <a name="dynamics-365-human-resources-entities"></a>เอนทิตี้ Dynamics 365 Human Resources

เอนทิตี้ต่อไปนี้สำหรับ Dynamics 365 Human Resources จะแสดงรายการตามลำดับที่คุณควรเปิดใช้งาน

| ชื่อการแม็ปในหน้าการรวมแบบสองทิศทาง | ชื่อข้อมูลเมตาของเอนทิตี้ใน Human Resources | ชื่อข้อมูลเมตาของเอนทิตี้ใน Common Data Service | หมายเหตุ |
|---|---|---|---|
| cdm_jobfunction - ฟังก์ชันงาน                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - ชนิดงาน                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - งาน                                               |                                   | cdm_jobs                         | |
| cdm_jobs - รายละเอียดงาน                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - ชนิดตำแหน่ง                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - ตำแหน่งฐาน                              | HcmPositionBaseEntity             | cdm_jobposition                  | ดู [หมายเหตุ 1](#hr-notes) |
| cdm_jobposition - รายละเอียดตำแหน่ง                            | HcmPositionDetailEntity           | cdm_jobposition                  | ดู [หมายเหตุ 1](#hr-notes) |
| cdm_jobposition - ระยะเวลาของตำแหน่ง                           | HcmPositionDurationEntity         | cdm_jobposition                  | ดู [หมายเหตุ 1](#hr-notes) |
| cdm_jobposition - ดับชั้นของตำแหน่ง                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | ดู [หมายเหตุ 1](#hr-notes) |
| cdm_veteranstatus - สถานะทหารผ่านศึก                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - เชื้อชาติ                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - รหัสภาษา                              |                                   | cdm_languagecode                 | |
| cdm_worker - ผู้ปฏิบัติงาน                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - การจ้างงาน                                 |                                   | cdm_employments                  | |
| cdm_employments - รายละเอียดการจ้างงาน                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - การกำหนดตำแหน่งของผู้ปฏิบัติงาน | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | ดู [หมายเหตุ 2](#hr-notes)|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>หมายเหตุเฉพาะการแม็ป

1. เอนทิตี้ของ Common Data Service หนึ่งเอนทิตี้จะได้รับการแม็ปกับหลายเอนทิตี้ของแอป Finance and Operations
2. การแม็ปนี้มีการอ้างอิงตนเอง

## <a name="asset-management-entities"></a>เอนทิตี้การจัดการสินทรัพย์

เอนทิตี้ต่อไปนี้ของการจัดการสินทรัพย์สำหรับ Dynamics 365 Supply Chain Management จะแสดงรายการตามลำดับที่คุณควรเปิดใช้งาน

| ชื่อการแม็ปในหน้าการรวมแบบสองทิศทาง | ชื่อข้อมูลเมตาของเอนทิตี้ในการจัดการสินทรัพย์ | ชื่อข้อมูลเมตาของเอนทิตี้ใน Common Data Service | หมายเหตุ |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | สถานะของวงจรการใช้ของสินทรัพย์ในการจัดการสินทรัพย์               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | แบบจำลองวงจรการใช้งานของสินทรัพย์ในการจัดการสินทรัพย์               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | แบบจำลองวงจรการใช้งานของตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | สถานะของวงจรการใช้ของตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | ชนิดสินทรัพย์ในการจัดการสินทรัพย์                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | ชนิดของตำแหน่งที่ทำงานในการจัดการสินทรัพย์            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | ตำแหน่งที่ทำงานในการจัดการสินทรัพย์                 | msdyn_functionallocations                | ดู [หมายเหตุ](#am-notes) |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | สินทรัพย์ในการจัดการสินทรัพย์                               | msdyn_customerassets                     | ดู [หมายเหตุ](#am-notes) |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | ผู้ผลิตของการจัดการสินทรัพย์                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | แบบจำลองการจัดการสินทรัพย์                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | การรับประกันของการจัดการสินทรัพย์                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>หมายเหตุเฉพาะการแม็ป

- เนื่องจากเป็นการอ้างอิงตนเอง คุณอาจต้องเรียกใช้การซิงโครไนส์เริ่มแรกมากกว่าหนึ่งครั้ง
