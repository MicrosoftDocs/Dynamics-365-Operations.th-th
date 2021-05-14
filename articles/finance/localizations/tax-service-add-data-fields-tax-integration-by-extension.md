---
title: เพิ่มฟิลด์ข้อมูลในการรวมภาษีโดยใช้ส่วนขยาย
description: หัวข้อนี้อธิบายวิธีการใช้ส่วนขยาย X++ เพื่อเพิ่มฟิลด์ข้อมูลในการรวมภาษี
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8e3573f9c9971d4a5af33ece08b7e0b43f2e813a
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921176"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="668b9-103">เพิ่มฟิลด์ข้อมูลในการรวมภาษีโดยใช้ส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="668b9-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="668b9-104">หัวข้อนี้อธิบายวิธีการใช้ส่วนขยาย X++ เพื่อเพิ่มฟิลด์ข้อมูลในการรวมภาษี</span><span class="sxs-lookup"><span data-stu-id="668b9-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="668b9-105">ฟิลด์เหล่านี้สามารถขยายไปยังรูปแบบข้อมูลภาษีของบริการภาษี และใช้เพื่อระบุรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="668b9-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="668b9-106">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฟิลด์เพิ่มข้อมูลในการตั้งค่าคอนฟิกภาษี](tax-service-add-data-fields-tax-configurations.md)</span><span class="sxs-lookup"><span data-stu-id="668b9-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="668b9-107">แบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-107">Data model</span></span>

<span data-ttu-id="668b9-108">ข้อมูลในรูปแบบข้อมูลจะมีการดําเนินการโดยออบเจ็กต์และใช้งานโดยคลาส</span><span class="sxs-lookup"><span data-stu-id="668b9-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="668b9-109">ต่อไปนี้เป็นรายการของออบเจ็กต์หลัก:</span><span class="sxs-lookup"><span data-stu-id="668b9-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="668b9-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="668b9-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="668b9-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="668b9-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="668b9-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="668b9-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="668b9-113">รูปภาพประกอบต่อไปนี้แสดงวิธีที่ออบเจ็กต์เหล่านี้เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="668b9-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="668b9-114">[![ความสัมพันธ์ของออบเจ็กต์รูปแบบข้อมูล](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="668b9-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="668b9-115">ออบเจ็กต์ **เอกสาร** อาจประกอบด้วยออบเจ็กต์ **รายการ** หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="668b9-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="668b9-116">แต่ละออบเจ็กต์จะประกอบด้วยข้อมูลเมตาสำหรับบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="668b9-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="668b9-117">`TaxIntegrationDocumentObject` มีข้อมูลเมตา `originAddress` ซึ่งมีข้อมูลเกี่ยวกับที่อยู่ต้นทาง และข้อมูลเมตา `includingTax` ซึ่งบ่งชี้ว่ายอดเงินในรายการรวมภาษีขายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="668b9-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="668b9-118">`TaxIntegrationLineObject` มีข้อมูลเมตา `itemId`, `quantity` และ `categoryId`</span><span class="sxs-lookup"><span data-stu-id="668b9-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="668b9-119">`TaxIntegrationLineObject` ยังใช้ออบเจ็กต์ **ค่าธรรมเนียม** ด้วย</span><span class="sxs-lookup"><span data-stu-id="668b9-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="668b9-120">โฟลว์การรวม</span><span class="sxs-lookup"><span data-stu-id="668b9-120">Integration flow</span></span>

<span data-ttu-id="668b9-121">ข้อมูลในโฟลว์จะถูกจัดการโดยกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="668b9-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="668b9-122">กิจกรรมหลัก</span><span class="sxs-lookup"><span data-stu-id="668b9-122">Key activities</span></span>

* <span data-ttu-id="668b9-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="668b9-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="668b9-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="668b9-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="668b9-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="668b9-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="668b9-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="668b9-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="668b9-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="668b9-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="668b9-128">กิจกรรมจะรันตามลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="668b9-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="668b9-129">การดึงข้อมูลการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="668b9-129">Setting Retrieval</span></span>
2. <span data-ttu-id="668b9-130">การดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-130">Data Retrieval</span></span>
3. <span data-ttu-id="668b9-131">บริการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="668b9-131">Calculation Service</span></span>
4. <span data-ttu-id="668b9-132">การแลกเปลี่ยนสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="668b9-132">Currency Exchange</span></span>
5. <span data-ttu-id="668b9-133">การยังคงอยู่ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-133">Data Persistence</span></span>

<span data-ttu-id="668b9-134">ตัวอย่างเช่น ขยาย **การดึงข้อมูล** ก่อน **บริการคํานวณ**</span><span class="sxs-lookup"><span data-stu-id="668b9-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="668b9-135">กิจกรรมการดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-135">Data Retrieval activities</span></span>

<span data-ttu-id="668b9-136">กิจกรรม **การดึงข้อมูล** จะดึงข้อมูลจากฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="668b9-137">ตัวปรับต่อสำหรับธุรกรรมต่างๆ จะพร้อมใช้งานเพื่อดึงข้อมูลจากตารางธุรกรรมต่างๆ:</span><span class="sxs-lookup"><span data-stu-id="668b9-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="668b9-138">AxClass/TaxIntegration **PurchTable** DataRetarival</span><span class="sxs-lookup"><span data-stu-id="668b9-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="668b9-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="668b9-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="668b9-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="668b9-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="668b9-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="668b9-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="668b9-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="668b9-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="668b9-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="668b9-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="668b9-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="668b9-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="668b9-145">ในกิจกรรม **การดึงข้อมูล** เหล่านี้ ข้อมูลจะถูกคัดลอกจากฐานข้อมูลไปยัง `TaxIntegrationDocumentObject` และ `TaxIntegrationLineObject`</span><span class="sxs-lookup"><span data-stu-id="668b9-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="668b9-146">เนื่องจากกิจกรรมเหล่านี้ทั้งหมดขยายคลาสเท็มเพลตนามธรรมเดียวกัน จึงมีวิธีการที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="668b9-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="668b9-147">กิจกรรมการบริการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="668b9-147">Calculation Service activities</span></span>

<span data-ttu-id="668b9-148">กิจกรรม **บริการคํานวณ** คือลิงค์ระหว่างบริการภาษีและการรวมภาษี</span><span class="sxs-lookup"><span data-stu-id="668b9-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="668b9-149">กิจกรรมนี้จะรับผิดชอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="668b9-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="668b9-150">สร้างคำขอ</span><span class="sxs-lookup"><span data-stu-id="668b9-150">Construct the request.</span></span>
2. <span data-ttu-id="668b9-151">ลงรายการบัญชีการร้องขอไปยังบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="668b9-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="668b9-152">รับการตอบสนองจากบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="668b9-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="668b9-153">แยกวิเคราะห์การตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="668b9-153">Parse the response.</span></span>

<span data-ttu-id="668b9-154">ฟิลด์ข้อมูลที่คุณเพิ่มลงในการร้องขอ จะมีการลงรายการบัญชีพร้อมกับข้อมูลเมตาอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="668b9-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="668b9-155">การใช้งานส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="668b9-155">Extension implementation</span></span>

<span data-ttu-id="668b9-156">ส่วนนี้แสดงขั้นตอนโดยละเอียดที่อธิบายวิธีการใช้ส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="668b9-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="668b9-157">ซึ่งจะใช้มิติทางการเงิน **ศูนย์ต้นทุน** และ **โครงการ** เป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="668b9-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="668b9-158">ขั้นตอนที่ 1</span><span class="sxs-lookup"><span data-stu-id="668b9-158">Step 1.</span></span> <span data-ttu-id="668b9-159">เพิ่มตัวแปรข้อมูลในคลาสออบเจ็กต์</span><span class="sxs-lookup"><span data-stu-id="668b9-159">Add the data variable in the object class</span></span>

<span data-ttu-id="668b9-160">คลาสออบเจ็กต์ประกอบด้วยตัวแปรข้อมูลและวิธีการของตัวรับ/ตัวเซ็ตสำหรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="668b9-161">เพิ่มฟิลด์ข้อมูลไปยัง `TaxIntegrationDocumentObject` หรือ `TaxIntegrationLineObject` อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับระดับของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="668b9-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="668b9-162">ตัวอย่างต่อไปนี้ใช้ระดับรายการ และชื่อไฟล์คือ `TaxIntegrationLineObject_Extension.xpp`</span><span class="sxs-lookup"><span data-stu-id="668b9-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="668b9-163">ถ้าฟิลด์ข้อมูลที่คุณกำลังเพิ่มอยู่ในระดับเอกสาร ให้เปลี่ยนชื่อไฟล์เป็น `TaxIntegrationDocumentObject_Extension.xpp`</span><span class="sxs-lookup"><span data-stu-id="668b9-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="668b9-164">**ศูนย์ต้นทุน** และ **โครงการ** มีการเพิ่มเป็นตัวแปรส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="668b9-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="668b9-165">สร้างวิธีการของตัวรับ/ตัวเซ็ตสำหรับฟิลด์ข้อมูลเหล่านี้เพื่อจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="668b9-166">ขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="668b9-166">Step 2.</span></span> <span data-ttu-id="668b9-167">ดึงข้อมูลจากฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-167">Retrieve data from the database</span></span>

<span data-ttu-id="668b9-168">ระบุธุรกรรม และขยายคลาสตัวปรับต่อร์ที่เหมาะสมเพื่อดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="668b9-169">ตัวอย่างเช่น ถ้าคุณใช้ธุรกรรม **ใบสั่งซื้อ** คุณต้องขยาย `TaxIntegrationPurchTableDataRetrieval` และ `TaxIntegrationVendInvoiceInfoTableDataRetrieval`</span><span class="sxs-lookup"><span data-stu-id="668b9-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="668b9-170">`TaxIntegrationPurchParmTableDataRetrieval` สืบทอดมาจาก `TaxIntegrationPurchTableDataRetrieval`</span><span class="sxs-lookup"><span data-stu-id="668b9-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="668b9-171">ซึ่งไม่ควรเปลี่ยนแปลง นอกจากตรรกะของตาราง `purchTable` และ `purchParmTable` จะแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="668b9-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="668b9-172">ถ้าควรเพิ่มฟิลด์ข้อมูลสำหรับธุรกรรมทั้งหมด ให้ขยายคลาส `DataRetrieval` ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="668b9-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="668b9-173">เนื่องจากกิจกรรม **การดึงข้อมูล** ทั้งหมดขยายคลาสเท็มเพลตเดียวกัน โครงสร้างคลาส ตัวแปร และวิธีการจะคล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="668b9-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="668b9-174">ตัวอย่างต่อไปนี้จะแสดงโครงสร้างพื้นฐาน เมื่อมีการใช้ตาราง `PurchTable`</span><span class="sxs-lookup"><span data-stu-id="668b9-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="668b9-175">เมื่อมีการเรียกวิธีการ `CopyToDocument` บัฟเฟอร์ `this.purchTable` จะมีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="668b9-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="668b9-176">วัตถุประสงค์ของวิธีการนี้คือการคัดลอกข้อมูลที่ต้องใช้ทั้งหมดจาก `this.purchTable` ไปยังออบเจ็กต์ `document` โดยใช้วิธีการของตัวเซ็ตที่สร้างขึ้นในคลาส `DocumentObject`</span><span class="sxs-lookup"><span data-stu-id="668b9-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="668b9-177">เช่นเดียวกับที่มีบัฟเฟอร์ `this.purchLine` อยู่แล้วในวิธีการ `CopyToLine`</span><span class="sxs-lookup"><span data-stu-id="668b9-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="668b9-178">วัตถุประสงค์ของวิธีการนี้คือการคัดลอกข้อมูลที่ต้องใช้ทั้งหมดจาก `this.purchLine` ไปยังออบเจ็กต์ `_line` โดยใช้วิธีการของตัวเซ็ตที่สร้างขึ้นในคลาส `LineObject`</span><span class="sxs-lookup"><span data-stu-id="668b9-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="668b9-179">วิธีที่ตรงไปตรงมาที่สุดคือการขยายวิธีการ `CopyToDocument` และ `CopyToLine`</span><span class="sxs-lookup"><span data-stu-id="668b9-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="668b9-180">อย่างไรก็ตาม เราขอแนะนำว่าคุณควรลองใช้วิธีการ `copyToDocumentFromHeaderTable` และ `copyToLineFromLineTable` ก่อน</span><span class="sxs-lookup"><span data-stu-id="668b9-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="668b9-181">หากไม่ทำงานตามที่คุณต้องการ ให้ใช้วิธีการของคุณเอง และเรียกใน `CopyToDocument` และ `CopyToLine`</span><span class="sxs-lookup"><span data-stu-id="668b9-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="668b9-182">มีสถานการณ์ทั่วไปสามสถานการณ์ที่คุณอาจใช้วิธีการนี้:</span><span class="sxs-lookup"><span data-stu-id="668b9-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="668b9-183">ฟิลด์ที่ต้องใช้อยู่ใน `PurchTable` หรือ `PurchLine`</span><span class="sxs-lookup"><span data-stu-id="668b9-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="668b9-184">ในสถานการณ์นี้ คุณสามารถขยาย `copyToDocumentFromHeaderTable` และ `copyToLineFromLineTable`</span><span class="sxs-lookup"><span data-stu-id="668b9-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="668b9-185">ต่อไปนี้เป็นรหัสตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="668b9-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="668b9-186">ข้อมูลที่ต้องใช้ไม่อยู่ในตารางเริ่มต้นของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="668b9-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="668b9-187">อย่างไรก็ตาม มีความสัมพันธ์ตัวเชื่อมบางความสัมพันธ์กับตารางเริ่มต้น และต้องใช้ฟิลด์ในรายการส่วนใหญ่</span><span class="sxs-lookup"><span data-stu-id="668b9-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="668b9-188">ในสถานการณ์นี้ ให้แทนที่ `getDocumentQueryObject` หรือ `getLineObject` เพื่อสอบถามตารางด้วยความสัมพันธ์ตัวเชื่อม</span><span class="sxs-lookup"><span data-stu-id="668b9-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="668b9-189">ในตัวอย่างต่อไปนี้ ฟิลด์ **จัดส่งทันที** จะถูกรวมเข้ากับใบสั่งขายที่ระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="668b9-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="668b9-190">ในตัวอย่างนี้ มีการประกาศบัฟเฟอร์ `mcrSalesLineDropShipment` และมีการกําหนดการสอบถามใน `getLineQueryObject`</span><span class="sxs-lookup"><span data-stu-id="668b9-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="668b9-191">การสอบถามใช้ความสัมพันธ์ `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`</span><span class="sxs-lookup"><span data-stu-id="668b9-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="668b9-192">ขณะที่คุณกำลังขยายในสถานการณ์นี้ คุณสามารถแทนที่ `getLineQueryObject` ด้วยออบเจ็กต์การสอบถามที่สร้างขึ้นของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="668b9-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="668b9-193">อย่างไรก็ตาม บันทึกจุดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="668b9-193">However, note the following points:</span></span>

    * <span data-ttu-id="668b9-194">เนื่องจากค่าที่ส่งคืนของวิธีการ `getLineQueryObject` คือ `SysDaQueryObject` คุณต้องสร้างออบเจ็กต์นี้โดยใช้วิธีการ SysDa</span><span class="sxs-lookup"><span data-stu-id="668b9-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="668b9-195">ไม่สามารถลบตารางที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="668b9-195">Can't remove existed table.</span></span>

- <span data-ttu-id="668b9-196">ข้อมูลที่ต้องใช้เกี่ยวข้องกับตารางธุรกรรมโดยความสัมพันธ์ตัวเชื่อมที่ซับซ้อน หรือความสัมพันธ์ไม่ใช่ความสัมพันธ์แบบหนึ่งต่อหนึ่ง (1:1) แต่เป็นความสัมพันธ์แบบหนึ่งต่อกลุ่ม (1:N)</span><span class="sxs-lookup"><span data-stu-id="668b9-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="668b9-197">ในสถานการณ์นี้ สิ่งต่างๆ จะซับซ้อนเล็กน้อย</span><span class="sxs-lookup"><span data-stu-id="668b9-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="668b9-198">สถานการณ์นี้จะใช้กับตัวอย่างของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="668b9-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="668b9-199">ในสถานการณ์นี้ คุณสามารถใช้วิธีการของคุณเองเพื่อดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="668b9-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="668b9-200">ต่อไปนี้เป็นรหัสตัวอย่างในไฟล์ `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`</span><span class="sxs-lookup"><span data-stu-id="668b9-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="668b9-201">ขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="668b9-201">Step 3.</span></span> <span data-ttu-id="668b9-202">เพิ่มข้อมูลในการร้องขอ</span><span class="sxs-lookup"><span data-stu-id="668b9-202">Add data to the request</span></span>

<span data-ttu-id="668b9-203">ขยายวิธีการ `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` หรือ `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` เพื่อเพิ่มข้อมูลในการร้องขอ</span><span class="sxs-lookup"><span data-stu-id="668b9-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="668b9-204">ต่อไปนี้เป็นรหัสตัวอย่างในไฟล์ `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`</span><span class="sxs-lookup"><span data-stu-id="668b9-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="668b9-205">ในรหัสนี้ `_destination` เป็นออบเจ็กต์ตัวตัดคำที่ใช้ในการสร้างการร้องขอการลงรายการบัญชี และ `_source` เป็นออบเจ็กต์ `TaxIntegrationLineObject`</span><span class="sxs-lookup"><span data-stu-id="668b9-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="668b9-206">กําหนดคีย์ที่จะใช้ในฟอร์มการร้องขอเป็น `private const str`</span><span class="sxs-lookup"><span data-stu-id="668b9-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="668b9-207">ตั้งค่าฟิลด์ในวิธีการ `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` โดยใช้วิธีการ `SetField`</span><span class="sxs-lookup"><span data-stu-id="668b9-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="668b9-208">ชนิดข้อมูลของพารามิเตอร์ที่สองควรเป็น `string`</span><span class="sxs-lookup"><span data-stu-id="668b9-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="668b9-209">ถ้าชนิดข้อมูลไม่ใช่ `string` ให้แปลงเป็น `string`</span><span class="sxs-lookup"><span data-stu-id="668b9-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="668b9-210">ภาคผนวก</span><span class="sxs-lookup"><span data-stu-id="668b9-210">Appendix</span></span>

<span data-ttu-id="668b9-211">ภาคผนวกนี้แสดงรหัสตัวอย่างที่สมบูรณ์ของการรวมของมิติทางการเงิน (**ศูนย์ต้นทุน** และ **โครงการ**) ที่ระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="668b9-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="668b9-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="668b9-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="668b9-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="668b9-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="668b9-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="668b9-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
