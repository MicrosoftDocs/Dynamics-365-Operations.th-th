---
title: ตั้งค่าโฟลว์ข้อมูลทางเลือกสำหรับคำแนะนำ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกสภาพแวดล้อม โดยโฟลว์ข้อมูลทางเลือกเพื่อให้ข้อมูลแก่บริการข้อแนะนะนา
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460171"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>ตั้งค่าโฟลว์ข้อมูลทางเลือกสำหรับคำแนะนำ

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกสภาพแวดล้อม โดยโฟลว์ข้อมูลทางเลือกเพื่อให้ข้อมูลแก่บริการข้อแนะนะนา

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>การเปรียบเทียบโฟลว์ข้อมูลแบบสำเร็จรูป กับโฟลว์ข้อมูลทางเลือก

ภาพประกอบต่อไปนี้จะแสดงภาพโฟลว์ข้อมูลสำเร็จรูปในสภาพแวดล้อม

![โฟลว์ข้อมูลสำเร็จรูปในสภาพแวดล้อม](media/reco-out-of-the-box-dataflow-2.png)

ภาพต่อไปนี้อธิบายแสดงโฟลว์ข้อมูลทางเลือก ที่ซึ่งเอนทิตี้ที่จัดเก็บชุดงานการซิงค์ถูกแทนที่ด้วยโฟลว์ข้อมูลทางเลือก

![โฟลว์ข้อมูลทางเลือกในสภาพแวดล้อม](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>สมมติฐาน

- บทความนี้สันนิษฐานว่าคุณได้เปิดใช้งานบริการค่าแนะนะอธิบายไว้อยู่แล้วในสภาพแวดล้อมของคุณ สำหรับข้อมูลเพิ่มเติม ดูที่ [เปิดใช้งานการแนะนำผลิตภัณฑ์](enable-product-recommendations.md)
- เมื่อคุณใช้งานไฟล์และโฟลเดอร์ในบัญชี Microsoft Azure Data Lake storage:

    - คุณสามารถใช้อินเทอร์เฟสของเว็บพอร์ทัล Azure หรือแอปพลิเคชัน Azure Storage Explorer
    - จุดเริ่มต้นที่ใช้งานได้กับไฟล์และโฟลเดอร์อยู่ในคอนเทนเนอร์ **dynamics365-financeandoperations** ที่อยู่ภายใต้โฟลเดอร์ที่มีชื่อตรงกับ URL สภาพแวดล้อมของคุณ
    - ถ้าชื่อของสภาพแวดล้อม Sandbox ของคุณคือ **MyUAT** URL ฐานของสภาพแวดล้อมจะเป็น `myuat.sandbox.operations.dynamics.com`
    - ถ้ามากกว่าหนึ่งสภาพแวดล้อมเชื่อมต่อกับบัญชีที่จัดเก็บเดียวกัน แต่ละสภาพแวดล้อมจะมีโฟลเดอร์รากของตนเอง

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ข้อกำหนดเบื้องต้นต่อไปนี้ต้องตรงกัน ก่อนที่คุณจะสามารถดำเนินการโฟลว์ข้อมูลทางเลือก

### <a name="set-up-microsoft-power-platform"></a>ตั้งค่า Microsoft Power Platform

การตั้งค่า Microsoft Power Platform ให้ปฏิบัติตามคําแนะนําใน [เปิดใช้งานการรวม Microsoft Power Platform](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md)

### <a name="install-the-export-to-data-lake-add-in"></a>ติดตั้ง Add-in ของการส่งออกไปยัง Data Lake

การติดตั้ง Add-in ของการส่งออกไปยัง Data Lake ให้ทำตามคำแนะนำ [ติดตั้ง Add-in ของการส่งออกไปยัง Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)

> [!NOTE]
> บันทึกค่าคอนฟิกไว้ เนื่องจากคุณจะต้องใช้ค่าดังกล่าวในขั้นตอนต่างๆ ที่ตามมา

### <a name="configure-tables-to-export-in-dynamics-365"></a>การตั้งค่าคอนฟิกตารางที่จะส่งออกใน Dynamics 365

การซิงโครไนส์ตารางจาก Dynamics 365 Azure Data Lake Storage ได้รับการจัดการบนหน้า **ส่งออกไปยัง Data Lake** เนื่องจากขณะนี้หน้าไม่มีรายการเมนู เฉพาะผู้ใช้ในบทบาทความปลอดภัยของ **ผู้ดูแลระบบ** เท่านั้นที่สามารถเปิดได้

การตั้งค่าคอนฟิกตารางเพื่อส่งออกใน Dynamics 365 ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. เมื่อต้องการเปิดหน้า **ส่งออกไปยัง Data Lake** ให้เพิ่มสตริง `?mi=DataFeedsDefinitionWorkspace` ไปยัง URL พื้นฐานของสภาพแวดล้อม ดังที่แสดงในตัวอย่างต่อไปนี้:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. ในหน้า **ส่งออกไปยัง Data Lake** และคัดลอกตารางที่แสดงอยู่ในส่วน [ตารางคิวบ์รายการ RetailSales](#list-of-retailsales-cube-tables) ของบทความนี้
1. ในคอลัมน์ **ชื่อระบบ** ให้ขยายรายการของตัวเลือกตัวกรอง
1. สำหรับชนิดของตัวกรอง ให้เลือก **เป็นหนึ่งใน** แล้ววางเคอร์เซอร์ลงในกล่องข้อความ และวางรายการตารางที่คุณคัดลอกจากหน้า **ส่งออกไปยัง Data Lake**
1. ที่ด้านล่างของรายการตัวเลือกตัวกรอง ให้เลือก **นำไปใช้**
1. เลือกแถวทั้งหมดในกริด แล้วเลือก **เปิดใช้งาน**

> [!NOTE]
> ก่อนที่คุณจะย้ายไปที่ขั้นตอนถัดไป ต้องอัปเดตแถวทั้งหมดเป็นสถานะ **กำลังรัน** แก้ไขปัญหาและแก้ไขข้อผิดพลาดใดๆ ตามที่ต้องการ

### <a name="create-a-synapse-workspace"></a>สร้างพื้นที่ทำงาน Synapse

การสร้างพื้นที่งาน Synapsy ถ้าคุณไม่ได้มีอยู่แล้ว ให้ปฏิบัติตามคําแนะนําใน [เริ่มต้นใช้งานด่วน: สร้างพื้นที่งาน Synapse](/azure/synapse-analytics/quickstart-create-workspace)

การรักษาทรัพยากร Azure ให้จัดระเบียบไว้ เราขอแนะนาว่าคุณควรวางบัญชี Data Lake Storage และ พื้นที่ทำงาน Synaps เข้าด้วยกันในกลุ่มทรัพยากรใน Azure คุณสามารถใช้บัญชีที่จัดเก็บที่คุณสร้างขึ้นเมื่อคุณติดตั้ง Add in ส่งออกไปยัง Data Lake

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>สร้างฐานข้อมูลใน Synapsy เพื่อประมวลผลข้อมูลการแนะนา

ใช้แอปพลิเคชันคอนโซลยูทิลิตี Common Data Model (CDMUtil_ConsoleApp) เพื่อสร้างฐานข้อมูลในพื้นที่งาน Synapse ของคุณ และเติมข้อมูลจากตาราง Common Data Model ใน Data Lake Storage เราขอแนะให้ใช้ยูทิลิตี Common Data Model กับฐานข้อมูลของคุณในสภาพแวดล้อมการพัฒนา ในกรณีที่มีส่วนขยายใดๆ

> [!NOTE]
> ขั้นตอนต่อไปนี้สมมติว่าไม่มีการเพิ่มข้อมูลส่วนขยายใดในคิวบ์ RetailSales

การสร้างฐานข้อมูลใน Synapse ให้ทำตามขึ้นตอนเหล่านี้

1. ไปที่ [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) และปฏิบัติตามขั้นตอนเพื่อดาวน์โหลดไฟล์ **CDMUtilConsoleApp.zip**
1. แยกไฟล์ zip ลงในโฟลเดอร์เฉพาะที่
1. เปิดไฟล์ **CDMUtil_ConsoleApp.dll.config** ในตัวแก้ไขข้อความ และอัปเดตค่าต่อไปนี้:

    1. ตั้งค่า **รหัสผู้เช่า** (รหัสผู้เช่า Azure)
    1. ตั้งค่า **คีย์การเข้าถึง** (คีย์การเข้าถึงส้หรับบัญชี Data Lake Storage)

        1. ในพอร์ทัล Azure ให้เปิดบัญชีที่จัดเก็บของคุณ
        1. บนเมนูทางด้านซ้ายของหน้า ให้เลือก **คีย์การเข้าถึง**
        1. ที่ด้านบนของหน้า ให้เลือก **แสดงคีย์**
        1. เลือกปุ่มคัดลอกของฟิลด์คีย์ตัวใดตัวหนึ่งจากสองฟิลด์ แล้ววางค่าระหว่างเครื่องหมายอัญประกาศในไฟล์การตั้งค่าคอนฟิก

    1. ตั้งค่า **ManifestURL** เป็น URL ของไฟล์ **Tables.manifest.cdm.json** ใน Azure Data Lake Storage การรับ URL ให้เรียกดูไฟล์ในพอร์ทัล Azure เลือกจุดไข่ปลา (**...**) ทางด้านขวาของมุมมอง แล้วเลือก **คุณสมบัติ** URL เป็นคุณสมบัติแรกที่แสดงบนแท็บ **ภาพรวม**
    1. ตั้งค่า **TargetDbConnectionString** เป็นสตริงการเชื่อมต่อให้กับกลุ่ม SQL ที่ไม่มีเซิร์ฟเวอร์ในตัว ของพื้นที่ทำงาน Synapse ของคุณ

        1. ในพื้นที่ทำงานของ Synapse ให้เลือกแท็บ **จัดการ**
        1. บนเมนูย่อย ให้เลือก **กลุ่ม SQL**
        1. เลือกชื่อ **Built-in** เพื่อดูคุณสมบัติของกลุ่ม
        1. ในกล่องโต้ตอบคุณสมบัติ ให้เลือกชนิดการเชื่อมต่อ ADO.NET ที่คุณต้องการใช้ จากนั้นคัดลอกค่าสตริงการเชื่อมต่อ และวางระหว่างเครื่องหมายอัญประกาศในไฟล์การตั้งค่าคอนฟิก

        > [!NOTE]
        > คุณต้องมีสิทธิ์ในการสร้างงานฐานข้อมูล เพื่อให้การใช้งานง่ายขึ้น คุณอาจต้องการใช้บัญชีผู้ดูแลระบบ **sqladminuser** ในตัว

    1. ยกเลิกข้อคิดเห็นของโหนด **ProcessEntities** และตั้งค่าเป็น **จริง** (ตัวอย่างเช่น `<add key="ProcessEntities" value ="true"/>`)

1. บันทึกและปิดไฟล์ **CDMUtil_ConsoleApp.dll.config**
1. คัดลอกไฟล์ **EntityList.json** ไปยังไดเรกทอรี **/Manifest**
1. ในหน้าต่างพร้อมต์คำสั่ง ให้รัน **cdmutil_consoleapp.exe**

> [!NOTE]
> เมื่อคุณตรวจทานผลลัพธ์ ควรจะมีเอนทิตี้/มุมมอง 35 รายการ ตารางอย่างน้อย 75 ตาราง และไม่มีข้อผิดพลาด

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>จัดเตรียมไดเรกทอรีการวัดแบบรวมของ Data Lake RetailSales

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>ทำสำเนาข้อมูลคิวบ์ RetailSales ปัจจุบันของคุณจาก Data Lake Storage

วิธีที่ง่ายที่สุดในการสํารองข้อมูลคิวบ์ RetailSales ปัจจะบันของคุณ คือการเปลี่ยนชื่อไดเรกทอรี **RetailSales** ใน Data Lake Storage **RetailSales-backup** หรือที่คล้ายกัน วิธีการนี้จะเก็บรักษาข้อมูลที่มีอยู่ในกรณีที่ต้องใช้การแก้ไขปัญหาเบื้องต้นในภายหลัง

โฟลเดอร์คิวบ์ **/RetailSales** พบได้ในที่ตั้งต่อไปนี้:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>สร้างโฟลเดอร์ RetailSales ใหม่ และอัปโหลดไฟล์โมเดล

หากต้องการสร้างไดเรกทอรี **RetailSales** ใหม่และอัปโหลดไฟล์ **model.json** ไปยัง Data Lake Storage ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. สร้างไดเรกทอรีเปล่าขึ้นใหม่ที่ระดับเดียวกับไดเรกทอรีก่อนหน้านี้ และตั้งชื่อเป็น **RetailSales**
1. อัปโหลดไฟล์ **model.json** ไปยังไดเรกทอรีใหม่

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>สร้างไปป์ไลน์เพื่อคัดลอกข้อมูลคิวบ์ RetailSales

ไปป์ไลน์จะอ่านมุมมองคิวบ์ RetailSales และส่งออกข้อมูลไปยังไฟล์ .csv ใน Data Lake Storage

การสร้างไปป์ไลน์เพื่อคัดลอกข้อมูลคิวบ์ RetailSales ให้ทำตารมขั้นตอนเหล่านี้

1. ในพื้นที่ทำงาน Synapse ให้เลือกแท็บ **รวม**
1. เลือกเครื่องหมายบวก (**+**) แล้วเลือก **นำเข้าจากเทมเพลตไปป์ไลน์**
1. ดาวน์โหลดแล้วเลือก [ไฟล์ ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files)
1. เลือกบริการที่เชื่อมโยงฐานข้อมูล SQL ของคุณ
1. เลือกบริการที่เชื่อมโยงบัญชีการจัดเก็บของคุณ
1. เปิดเครื่องมือ **คัดลอกข้อมูล** และเปลี่ยนคุณสมบัติ **พาธโฟลเดอร์** เป็น **\<environment_name\>/...**

### <a name="test-execution-of-the-pipeline"></a>การดำเนินการทดสอบไปป์ไลน์

ขอแนะนาว่าคุณควรทดสอบไปป์ไลน์โดยใช้มุมมองเดียว มุมมอง **RetailSales_RetailMediaTemplateView** ใช้ได้ เนื่องจากโดยปกติแล้วมุมมองนี้จะมีแถวน้อยกว่า 10 แถว

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>จัดกำหนดการไปป์ไลน์ที่จะรันบนกำหนดการที่เกิดขึ้นซ้ำ

ทุกครั้งที่ไปป์ไลน์รัน ปริมาณการใช้ Azure จะเกิดขึ้น เราขอแนะนาให้คุณจัดกำหนดการในช่วงเวลา 48 ชั่วโมง หรือนานกว่า คุณสามารถรันไปป์ไลน์ด้วยตนเองได้เสมอ หากคุณต้องซิงค์ข้อมูลทันที 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>รายการตารางการซิงโครไนส์จาก Dynamics 365 ไปยัง Data Lake Storage

รายการตารางต่อไปนี้เป็นชุดย่อยของตารางทั้งหมดที่ต้องใช้สำหรับคิวบ์ RetailSales ทั้งหมด มีเพียง 15 มุมมองในคิวบ์ RetailSales เท่านั้นที่บริการข้อนะแนะนจะใช้ และรายการตารางที่ต้องใช้จะถูกกรองข้อมูลตามนั้น

### <a name="list-of-retailsales-cube-tables"></a>รายการตารางคิวบ์ RetailSales

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- แค็ตตาล็อก
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>ดูรายการพารามิเตอร์ที่จะส่งผ่านไปยังไปป์ไลน์ Synapse

รายการที่แบ่งด้วยเครื่องหมายจุลภาคต่อไปนี้มีมุมมองคิวบ์ RetailSales ที่ไปป์ไลน์จะดําเนินงาน "เลือก" จากนั้นจะคัดลอกผลลัพธ์ไปยังที่จัดเก็บ Data Lake Storage

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> พารามิเตอร์ไปป์ไลน์ต้องเป็นรายการชื่อมุมมองที่ถูกแยกด้วยเครื่องหมายจุลภาคเดียว ต้องไม่มีที่ว่างหรือการป้อนบรรทัด

## <a name="environment-specific-fixes"></a>การแก้ไขเฉพาะสภาพแวดล้อม

### <a name="retailchannelview-fix"></a>การแก้ไข RETAILCHANNELVIEW

มุมมอง **RETAILCHANNELVIEW** ประกอบด้วยจํานวนเต็มที่มีรหัสแบบฮาร์ด ซึ่งแสดงถึงองค์กรที่มีชนิดเป็น "ช่องทางการขายปลีก" ค่าจริงของชนิดสามารถเปลี่ยนจากสภาพแวดล้อมเป็นสภาพแวดล้อม หรือจากผู้เช่าไปยังผู้เช่า

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

เพื่อปรับปรุงจํานวนเต็มที่มีรหัสแบบฮาร์ด ให้ดำเนินการตามขั้นตอนเหล่านี้

1. ใน Dynamics 365 ให้ค้นหาค่า **ChannelID** ของช่องทางออนไลน์ของคุณ
1. ในอินสแตนซ์ของ SQL Server Management Studio (SSMS) ที่แนบกับฐานข้อมูล Synapse ให้รันการสอบถามต่อไปนี้

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. คัดลอกค่าจากคอลัมน์แรก (**INSTANCERELATIONTYPE**) และวางลงในการกำหนดมุมมอง

## <a name="troubleshooting"></a>การแก้ไขปัญหา

### <a name="pipeline-task-fails"></a>งานไปป์ไลน์ล้มเหลว

ควรมีการปฏิบัติการงานไปป์ไลน์ 15 รายการสำหรับงาน **CopyData** หากการปฏิบัติการใดๆ ล้มเหลว คุณต้องตรวจสอบว่ามีออบเจ็กต์ SQL ที่ขึ้นต่อกันทั้งหมด และการสอบถามรันอยู่หรือไม่ วิธีที่ง่ายที่สุดในการเข้าถึงการขึ้นต่อกันทั้งหมดคือ การใช้ SSMS เพื่อเชื่อมต่อกับฐานข้อมูล คุณสามารถเลือกและระงับ (หรือคลิกขวา) มุมมอง และเลือก **สร้าง CREATE ในหน้าต่างใหม่**

ข้อความแสดงข้อผิดพลาดอาจรวมถึงข้อความต่อไปนี้:

- ข้อผิดพลาด: ล้มเหลวในฝั่ง 'ต้นทาง'
- ข้อผิดพลาดในการจัดการไฟล์ภายนอก: 'การตรวจนับข้อผิดพลาดสูงสุด'
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>ตัวอย่างสถานการณ์จำลอง

ในตัวอย่างนี้ งาน **RetailSales_RetailProductCategory** ที่ล้มเหลว และคุณจะได้รับข้อผิดพลาด "การตรวจนับข้อผิดพลาดสูงสุด"

การแก้ไขข้อผิดพลาด ทำตามขั้นตอนเหล่านี้

1. เปิดไฟล์ **EntityList.json** ในตัวแก้ไขข้อความ (ตัวอย่างเช่น Visual Studio Code)
1. ค้นหาข้อกำหนดมุมมอง **RetailSales_RetailProductCategory**

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. มุมมองนี้จะขึ้นอยู่กับมุมมองอื่นเพียงมุมมองเดียว: **RetailProductCategoryView** _ ค้นหาข้อกำหนดมุมมอง _*RetailProductCategoryView**

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. มุมมองนี้จะขึ้นอยู่กับมุมมองอื่นๆ สามมุมมองดังนี้: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** และ **RETAILCATEGORYEXPANDED** ค้นหาข้อกำหนดของแต่ละมุมมองเหล่านี้ และแสดงรายการการขึ้นต่อกัน ต่อไปจนกว่าคุณจะพบมุมมองที่ขึ้นต่อกันทั้งหมด

    ต่อไปนี้เป็นรายการทั้งหมดในลำดับแผนภูมิการขึ้นต่อกัน ต้องตรวจสอบความถูกต้องของมุมมองทั้งสิบสาม

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. ใน Excel ให้สร้างคำสั่ง **เลือกจำนวน(\*) จาก \<view_name\>** 13 คำสั่ง รันคำสั่งเหล่านี้ใน SSMS และส่งผลลัพธ์ไปยังข้อความ จากนั้นเลื่อนผ่านผลลัพธ์เพื่อดูว่ามุมมองใดๆ ล้มเหลวหรือไม่ ข้อผิดพลาดเริ่มต้นจะแนะนำว่ามุมมองใดมุมมองหนึ่งจะล้มเหลวอย่างน้อยหนึ่งมุมมอง

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. วิธีการหนึ่งในการตรวจสอบความถูกต้องสิ่งที่คุณค้นหาอยู่ก็คือ สร้างมุมมองที่ขึ้นอยู่กับรากเพื่อสร้างข้อกำหนดมุมมองใน SSMS แล้วตรวจสอบว่ามีคอลัมน์ไฟล์ Azure Data Lake ที่ชื่อ **r.filepath** การแสดงคอลัมน์นี้จะบ่งชี้ว่ามุมมองที่คุณตรวจสอบอยู่คือการอ่านข้อมูลจาก Data Lake Storage

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce](enable-adls-environment.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"](shop-similar-looks.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เพิ่มคำแนะนำผลิตภัณฑ์ใน POS](product.md)

[เพิ่มคำแนะนำในหน้าจอธุรกรรม](add-recommendations-control-pos-screen.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่ระบุด้วยตนเอง](create-editorial-recommendation-lists.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
