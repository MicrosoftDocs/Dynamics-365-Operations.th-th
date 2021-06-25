---
title: แดชบอร์ดการจัดการการใช้งาน
description: หัวข้อนี้อธิบายวิธีการใช้แดชบอร์ดการจัดการการใช้งา เพื่อตรวจสอบการใช้งานบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์และยังคงสอดคล้องอยู่
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130517"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="dabca-103">แดชบอร์ดการจัดการการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="dabca-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dabca-104">แดชบอร์ด **การจัดการการใช้งาน** ช่วยคุณในการตรวจสอบการใช้บริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ และเนื่องจากจะช่วยให้องค์กรของคุณยังคงสอดคล้องกับการใช้งานรายเดือน</span><span class="sxs-lookup"><span data-stu-id="dabca-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="dabca-105">การปฏิบัติตามกฎระเบียบกําหนดโดยการคํานวณปริมาณการส่งและการเปรียบเทียบปริมาณกับปริมาณการส่งที่ได้มาเพื่อระบุความเบี่ยงเบนใดๆ ระหว่างปริมาณที่ซื้อมาและปริมาณที่ใช้</span><span class="sxs-lookup"><span data-stu-id="dabca-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="dabca-106">แดชบอร์ดรวมถึงตัวระบุดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="dabca-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="dabca-107">ตัวบ่งชี้ต้นทุนหนึ่งที่คุณสามารถใช้ในการตรวจสอบปริมาณการใช้เพื่อวัตถุประสงค์ในการปฏิบัติตามกฎระเบียบการให้ลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="dabca-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="dabca-108">การใช้งานต่อเดือน (ส่งออก)</span><span class="sxs-lookup"><span data-stu-id="dabca-108">Usage per month (export)</span></span>

- <span data-ttu-id="dabca-109">ตัวบ่งชี้การปฏิบัติการสามตัวบ่งชี้ที่คุณสามารถใช้ในการติดตามการใช้งานบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เพื่อวัตถุประสงค์ในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="dabca-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="dabca-110">การใช้งานตามคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="dabca-110">Usage by feature</span></span>
    - <span data-ttu-id="dabca-111">การใช้งานตามสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="dabca-111">Usage by environment</span></span>
    - <span data-ttu-id="dabca-112">การใช้งานต่อเดือน (นำเข้า)</span><span class="sxs-lookup"><span data-stu-id="dabca-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="dabca-113">ขอบเขตการวัด</span><span class="sxs-lookup"><span data-stu-id="dabca-113">Measurement scope</span></span>

- <span data-ttu-id="dabca-114">หน่วยวัด:</span><span class="sxs-lookup"><span data-stu-id="dabca-114">Unit of measure:</span></span> 

    <span data-ttu-id="dabca-115">แดชบอร์ด **การจัดการการใช้งาน** จะนับการส่งเอกสารทางธุรกิจและใบแจ้งหนี้อิเล็กทรอนิกส์ที่นําเข้า</span><span class="sxs-lookup"><span data-stu-id="dabca-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="dabca-116">องค์กร:</span><span class="sxs-lookup"><span data-stu-id="dabca-116">Organization:</span></span> 

    <span data-ttu-id="dabca-117">การตรวจนับจะสรุปโดยรหัสผู้เช่าขององค์กรของคุณ ไม่ว่าจํานวนอินสแตนซ์ของ Microsoft Dynamics 365 Finance หรือ Dynamics 365 Supply Chain Management หรือจำนวนนิติบุคคลที่เปิดใช้งานบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์เท่าใด</span><span class="sxs-lookup"><span data-stu-id="dabca-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="dabca-118">ตัวบ่งชี้: การใช้ต่อเดือน (ส่งออก)</span><span class="sxs-lookup"><span data-stu-id="dabca-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="dabca-119">ตัวบ่งชี้นี้แสดงรายละเอียดเกี่ยวกับใบแจ้งหนี้อิเล็กทรอนิกส์ที่องค์กรของคุณออกใช้ในระหว่างรอบระยะเวลาที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="dabca-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="dabca-120">ขอบเขต</span><span class="sxs-lookup"><span data-stu-id="dabca-120">Scope</span></span>
- <span data-ttu-id="dabca-121">จํานวนเอกสารทางธุรกิจที่ส่งมาจากฝ่ายการเงินและ Supply Chain Management ไปยังบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ โดยไม่พิจารณาจํานวนรายการที่มีเอกสารทางธุรกิจดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="dabca-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="dabca-122">จํานวนเอกสารทางธุรกิจที่ส่งที่ประมวลผลโดยบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="dabca-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="dabca-123">เอกสารจะถือว่าเป็นประมวลผลเสร็จเรียบร้อยแล้ว เมื่อขั้นตอนของการกระบวนการที่กําหนดไว้ในการตั้งค่าลักษณะการเสร็จงานเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="dabca-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="dabca-124">เมื่อส่งใบแจ้งหนี้อิเล็กทรอนิกส์ไปที่บริการเว็บภายนอก การตรวจนับจะไม่ขึ้นอยู่กับผลลัพธ์ของการประมวลผลบริการเว็บ (ยอมรับ ปฏิเสธ หรือเกิดข้อผิดพลาดการตรวจสอบความถูกต้องของเค้าร่าง)</span><span class="sxs-lookup"><span data-stu-id="dabca-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="dabca-125">หากบริการเว็บได้รับและตอบสนองต่อคำขอจากบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ การส่งจะถือเป็นการตรวจนับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dabca-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="dabca-126">**ข้อยกเว้น:** ไม่ได้ตรวจนับเอกสารทางธุรกิจ ถ้ามีการส่งเอกสารดังกล่าวใหม่จากฝ่ายการเงินและ Supply Chain Management ไปยังบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ เช่น ในสถานการณ์ที่การส่งเอกสารทางธุรกิจเดียวกันใหม่ต้องมีการเปลี่ยนแปลงสถานะของใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="dabca-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="dabca-127">ตัวอย่างเช่น การออกใบแจ้งหนี้อิเล็กทรอนิกส์ของบราซิล (เอกสารทางการเงิน) ถูกนับเป็นถูกต้อง แต่จะไม่นับคำขอการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="dabca-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="dabca-128">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="dabca-128">Calculation</span></span>

<span data-ttu-id="dabca-129">การคํานวณยอดดุลจะเป็นดังนี้</span><span class="sxs-lookup"><span data-stu-id="dabca-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="dabca-130">ยอดดุล = ฟรี + ที่ซื้อ – ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="dabca-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="dabca-131">ที่ใด:</span><span class="sxs-lookup"><span data-stu-id="dabca-131">Where:</span></span>

- <span data-ttu-id="dabca-132">ฟรี:</span><span class="sxs-lookup"><span data-stu-id="dabca-132">Free:</span></span>
  
    <span data-ttu-id="dabca-133">ปริมาณเอกสารทางธุรกิจที่ลูกค้าสามารถส่งได้ต่อเดือนฟรี</span><span class="sxs-lookup"><span data-stu-id="dabca-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="dabca-134">ซึ่งประกอบด้วยเอกสารทางธุรกิจ 100 ฉบับที่สามารถส่งไปยังบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ได้</span><span class="sxs-lookup"><span data-stu-id="dabca-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="dabca-135">ปริมาณฟรีไม่สะสมและยอดดุลคงเหลือใดๆ ไม่ได้ย้อนกลับไปที่รอบระยะเวลาถัดไป</span><span class="sxs-lookup"><span data-stu-id="dabca-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="dabca-136">ซื้อแล้ว:</span><span class="sxs-lookup"><span data-stu-id="dabca-136">Purchased:</span></span>
  
    <span data-ttu-id="dabca-137">เอกสารทางธุรกิจ 1,000 ฉบับที่สามารถส่งไปยังบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ได้</span><span class="sxs-lookup"><span data-stu-id="dabca-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="dabca-138">แพคเกจนี้ต้องมีสำหรับองค์กรของคุณเป็นรายเดือน</span><span class="sxs-lookup"><span data-stu-id="dabca-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="dabca-139">ปริมาณที่ซื้อไม่สะสมและยอดดุลคงเหลือใดๆ ไม่ได้ย้อนกลับไปที่รอบระยะเวลาถัดไป</span><span class="sxs-lookup"><span data-stu-id="dabca-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="dabca-140">ใช้แล้ว:</span><span class="sxs-lookup"><span data-stu-id="dabca-140">Used:</span></span> 

    <span data-ttu-id="dabca-141">การตรวจนับการส่งเอกสารทางธุรกิจไปยังบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ตามเงื่อนไขที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="dabca-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="dabca-142">หากองค์กรของคุณวางแผนที่จะเกินปริมาณรายเดือน 100 การส่งฟรี ให้ซื้อปริมาณงานที่มีปริมาณงานสูงสุดเพื่อให้มั่นใจถึงความสอดคล้องตามนโยบายการให้ลิขสิทธิ์ของ Microsoft ในบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="dabca-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="dabca-143">ปริมาณที่ซื้อในปัจจุบันต้องถูกป้อนด้วยตนเอง ตามวันที่ซื้อสินทรัพย์ เนื่องจากแพคเกจหลายรายการคือ 1,000 รายการส่ง</span><span class="sxs-lookup"><span data-stu-id="dabca-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="dabca-144">ตัวบ่งชี้: การใช้งานตามคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="dabca-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="dabca-145">ตัวบ่งชี้นี้แสดงการใช้คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ของการออกใบแจ้งหนี้อิเล็กทรอนิกส์ในระหว่างรอบระยะเวลาที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="dabca-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="dabca-146">การคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="dabca-146">Calculation:</span></span>
  
    <span data-ttu-id="dabca-147">ที่ใช้ = การตรวจนับครั้งที่มีการใช้คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์แต่ละอย่าง ระหว่างการส่งเอกสารทางธุรกิจไปยังบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="dabca-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="dabca-148">ตัวบ่งชี้: การใช้งานตามสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="dabca-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="dabca-149">ตัวบ่งชี้นี้แสดงการใช้สภาพแวดล้อมบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ในระหว่างรอบระยะเวลาที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="dabca-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="dabca-150">การคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="dabca-150">Calculation:</span></span>
    
    <span data-ttu-id="dabca-151">ที่ใช้ = การตรวจนับครั้งที่มีการใช้สภาพแวดล้อมบริการการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์แต่ละอย่าง ระหว่างการส่งเอกสารทางธุรกิจไปยังบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="dabca-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="dabca-152">ตัวบ่งชี้: การใช้ต่อเดือน (นำเข้า)</span><span class="sxs-lookup"><span data-stu-id="dabca-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="dabca-153">ตัวบ่งชี้นี้แสดงปริมาณการนําเข้าใบแจ้งหนี้อิเล็กทรอนิกส์ โดยบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Finance และ Supply Chain Management ระหว่างรอบระยะเวลาที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="dabca-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="dabca-154">ขอบเขต:</span><span class="sxs-lookup"><span data-stu-id="dabca-154">Scope:</span></span>

    <span data-ttu-id="dabca-155">ใบแจ้งหนี้อิเล็กทรอนิกส์ที่นําเข้าไปยัง Finance และ Supply Chain Management ไม่ว่าจํานวนรายการในใบแจ้งหนี้อิเล็กทรอนิกส์เหล่านั้นจะประกอบด้วยรายการอย่างไรก็ตาม</span><span class="sxs-lookup"><span data-stu-id="dabca-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="dabca-156">การคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="dabca-156">Calculation:</span></span>

    <span data-ttu-id="dabca-157">ได้รับแล้ว = การตรวจนับของใบแจ้งหนี้อิเล็กทรอนิกส์ที่นําเข้าลงใน Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dabca-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="dabca-158">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="dabca-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="dabca-159">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="dabca-159">Purchase</span></span>

<span data-ttu-id="dabca-160">บนแท็บ **การใช้งานต่อเดือน (ส่งออก)** ให้เลือก **ซื้อ** เพื่อลงทะเบียนจํานวนเงินของการส่งที่ซื้อด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="dabca-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="dabca-161">ในวันที่ระบุ ให้เลือก **สร้าง** และป้อนจํานวน **แพคเกจ** ที่ซื้อมาในวันที่นั้น</span><span class="sxs-lookup"><span data-stu-id="dabca-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="dabca-162">**ปริมาณ** จะคำนวณตาม:</span><span class="sxs-lookup"><span data-stu-id="dabca-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="dabca-163">ปริมาณ =แพคเกจ \* 1.000</span><span class="sxs-lookup"><span data-stu-id="dabca-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="dabca-164">**ปริมาณ** ที่คํานวณได้จะสะท้อนถึง **ที่ซื้อ** จากตัวบ่งชี้ **การใช้ต่อเดือน (ส่งออก)**</span><span class="sxs-lookup"><span data-stu-id="dabca-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="dabca-165">อัพเดต</span><span class="sxs-lookup"><span data-stu-id="dabca-165">Update</span></span>

<span data-ttu-id="dabca-166">ในบานหน้าต่างการคํานวณ ให้เลือก **อัปเดต** เพื่อรีเฟรชการคํานวณและอัปเดตข้อมูลที่แสดงบนหน้าและในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="dabca-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="dabca-167">รีเซ็ตข้อมูลประวัติ</span><span class="sxs-lookup"><span data-stu-id="dabca-167">Reset history data</span></span>

<span data-ttu-id="dabca-168">ในบานหน้าต่างการดำเนินการ ให้เลือก **รีเซ็ตข้อมูลประวัติ** เพื่อรีเฟรชฐานข้อมูลที่คํานวณตัวบ่งชี้</span><span class="sxs-lookup"><span data-stu-id="dabca-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="dabca-169">แดชบอร์ด **การจัดการการใช้** จะไม่แสดงยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="dabca-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="dabca-170">แต่แสดงปริมาณการส่งที่ตรวจนับและเอกสารที่นําเข้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="dabca-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
