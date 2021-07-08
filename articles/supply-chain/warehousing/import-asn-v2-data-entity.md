---
title: นําเข้า ASN ขาเข้าผ่านเอนทิตีข้อมูล V2
description: หัวข้อนี้อธิบายวิธีการจัดการนําเข้าประกาศการจัดส่งสินค้าขั้นสูงขาเข้า (ASN) โดยผ่านเอนทิตีข้อมูล ASN V2 ขาเข้า
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249177"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="5a913-103">นําเข้า ASN ขาเข้าผ่านเอนทิตีข้อมูล V2</span><span class="sxs-lookup"><span data-stu-id="5a913-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a913-104">การแจ้งเตือนการจัดส่งขั้นสูง (ASN) จะแจ้งให้ทราบเกี่ยวกับการจัดส่งสินค้าของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5a913-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="5a913-105">ซึ่งช่วยให้ผู้ส่งอธิบายถึงเนื้อหาของการจัดส่งสินค้าและข้อมูลเพิ่มเติมเกี่ยวกับการจัดส่งสินค้า เช่น สินค้าและบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5a913-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="5a913-106">ASN สามารถช่วยให้พนักงานคลังสินค้าทราบถึงสิ่งที่มาถึง</span><span class="sxs-lookup"><span data-stu-id="5a913-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="5a913-107">ดังนั้นจึงสามารถจัดเตรียมได้</span><span class="sxs-lookup"><span data-stu-id="5a913-107">Therefore, they can prepare.</span></span> <span data-ttu-id="5a913-108">นอกจากนี้ พนักงานคลังสินค้าสามารถใช้ ASN เพื่อจับคู่รายละเอียดของการจัดส่งกับใบสั่งซื้อที่เกี่ยวข้องที่สร้างขึ้นก่อนหน้านี้ได้</span><span class="sxs-lookup"><span data-stu-id="5a913-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="5a913-109">หัวข้อนี้จะแสดงถึงชุดของสถานการณ์จำลองที่แสดง โดยผ่านตัวอย่าง วิธีการทำงานกับไฟล์ ASN</span><span class="sxs-lookup"><span data-stu-id="5a913-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a913-110">การนําเข้า *ASN ขาเข้า* จะใช้กับสินค้าที่เปิดใช้งานเฉพาะกับการจัดการคลังสินค้าขั้นสูง (WMS) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5a913-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="5a913-111">ก่อนที่คุณจะได้รับ ASN ต้องมีการลงทะเบียนใบสั่งซื้อในระบบกับผู้จัดจำหน่ายที่ส่ง ASN นั้นไป</span><span class="sxs-lookup"><span data-stu-id="5a913-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="5a913-112">เอนทิตี ASN V2 ขาเข้า</span><span class="sxs-lookup"><span data-stu-id="5a913-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="5a913-113">คุณนําเข้า ASN ขาเข้าโดยใช้เอนทิตีข้อมูลแบบรวม *ASN V2 ขาเข้า*</span><span class="sxs-lookup"><span data-stu-id="5a913-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="5a913-114">*ASN V2 ขาเข้า* ใช้ประโยชน์จากเอนทิตีต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5a913-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="5a913-115">ส่วนหัวของการบรรทุกขาเข้า</span><span class="sxs-lookup"><span data-stu-id="5a913-115">Inbound load header</span></span>
- <span data-ttu-id="5a913-116">ส่วนหัวของการจัดส่งขาเข้า</span><span class="sxs-lookup"><span data-stu-id="5a913-116">Inbound shipment header</span></span>
- <span data-ttu-id="5a913-117">โครงสร้างการบรรจุโหลดขาเข้า</span><span class="sxs-lookup"><span data-stu-id="5a913-117">Inbound load packing structures</span></span>
- <span data-ttu-id="5a913-118">กล่องโครงสร้างการบรรจุโหลดขาเข้า</span><span class="sxs-lookup"><span data-stu-id="5a913-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="5a913-119">รายการกล่องโครงสร้างการบรรจุโหลดขาเข้า</span><span class="sxs-lookup"><span data-stu-id="5a913-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="5a913-120">รายการโครงสร้างการบรรจุโหลดขาเข้า</span><span class="sxs-lookup"><span data-stu-id="5a913-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="5a913-121">เอนทิตีข้อมูลแบบรวม *ASN V2 ขาเข้า* ที่ใช้กับสถานการณ์การรวมแบบอสมวารซึ่งใช้การนําเข้าโดยใช้ไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="5a913-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="5a913-122">รูปแบบ XML สำหรับการนําเข้า ASN</span><span class="sxs-lookup"><span data-stu-id="5a913-122">XML format for importing ASNs</span></span>

<span data-ttu-id="5a913-123">Microsoft Dynamics 365 Supply Chain Management สนับสนุนรูปแบบ XML ต่อไปนี้เพื่อนําเข้า ASN</span><span class="sxs-lookup"><span data-stu-id="5a913-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="5a913-124">แต่ละโหนดในไฟล์ XML แสดงถึงแอททริบิวต์จากแต่ละเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="5a913-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="5a913-125">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="5a913-125">Examples</span></span>

<span data-ttu-id="5a913-126">ส่วนย่อยต่อไปนี้แสดงตัวอย่างไฟล์นําเข้า ASN XML ของการจัดส่งของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5a913-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="5a913-127">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="5a913-127">Example 1</span></span>

<span data-ttu-id="5a913-128">ตัวอย่างต่อไปนี้แสดงไฟล์ XML ในการนําเข้าการจัดส่งของผู้จัดจำหน่ายในใบสั่งซื้อใบเดียวเมื่อไม่มีรายละเอียดกรณีรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="5a913-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="5a913-129">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="5a913-129">Example 2</span></span>

<span data-ttu-id="5a913-130">ตัวอย่างต่อไปนี้แสดงไฟล์ XML ในการนําเข้าการจัดส่งของผู้จัดจำหน่ายในใบสั่งซื้อใบเดียวเมื่อมีรายละเอียดกรณีรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="5a913-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="5a913-131">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="5a913-131">Example 3</span></span>

<span data-ttu-id="5a913-132">ตัวอย่างต่อไปนี้แสดงไฟล์ XML ในการนําเข้าการจัดส่งของผู้จัดจำหน่ายในใบสั่งซื้อหลายใบเมื่อมีรายละเอียดกรณีรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="5a913-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="5a913-133">ตรวจสอบผลลัพธ์ของการนําเข้าไฟล์ ASN</span><span class="sxs-lookup"><span data-stu-id="5a913-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="5a913-134">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตรวจสอบผลลัพธ์ของการนําเข้าไฟล์ ASN</span><span class="sxs-lookup"><span data-stu-id="5a913-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="5a913-135">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5a913-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5a913-136">ค้นหาและเปิดโหลดที่สร้างเป็นส่วนหนึ่งของการนําเข้า ASN</span><span class="sxs-lookup"><span data-stu-id="5a913-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="5a913-137">บนแท็บด่วน **โหลด** คุณควรจะเห็นค่าที่ขึ้นอยู่กับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="5a913-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="5a913-138">บนแท็บด่วน **รายการสินค้า** คุณควรจะเห็นหมายเลขใบสั่งซื้อและรายละเอียดสินค้าที่ขึ้นอยู่กับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="5a913-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="5a913-139">ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **การรับ** ให้เลือก **โครงสร้างการบรรจุ** เพื่อตรวจสอบโครงสร้างการบรรจุของปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="5a913-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="5a913-140">บนแท็บด่วน **แท่นวางสินค้า** คุณควรจะเห็นป้ายทะเบียนที่ขึ้นอยู่กับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="5a913-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="5a913-141">บนแท็บด่วน **กรณี** คุณควรจะเห็นกรณีที่ขึ้นอยู่กับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="5a913-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="5a913-142">บนแท็บด่วน **สินค้า** คุณควรจะเห็นสินค้าและปริมาณที่ขึ้นอยู่กับไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="5a913-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
