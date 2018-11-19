---
title: "การรวมทางการเงินสำหรับช่องทางการขายปลีก"
description: "หัวข้อนี้แสดงภาพรวมของการรวมทางการเงินสำหรับ Retail POS"
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: th-th
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="35eb2-103">การรวมทางการเงินสำหรับช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="35eb2-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35eb2-104">หัวข้อนี้เป็นภาพรวมของฟังก์ชันการรวมทางการเงินที่พร้อมใช้งานใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="35eb2-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="35eb2-105">ฟังก์ชันการรวมทางการเงินคือ กรอบงานที่ออกแบบมาเพื่อสนับสนุนกฎหมายทางเฉพาะที่ที่ถูกกำหนดเพื่อป้องกันการฉ้อโกงในอุตสาหกรรมค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="35eb2-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="35eb2-106">สถานการณ์ทั่วไปที่สามารถครอบคลุมโดยใช้การรวมทางการเงินประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="35eb2-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="35eb2-107">การพิมพ์ใบเสร็จทางการเงิน และการมอบแก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="35eb2-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="35eb2-108">การรักษาความปลอดภัยในการส่งข้อมูลที่เกี่ยวข้องกับการขายและการส่งคืนที่ทำบน POS ไปยังบริการภายนอกที่ให้โดยหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="35eb2-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="35eb2-109">การใช้การป้องกันข้อมูลด้วยลายเซ็นดิจิทัลที่ได้รับอนุญาตโดยหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="35eb2-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="35eb2-110">หัวข้อนี้ให้คำแนะนำสำหรับการตั้งค่าการรวมทางการเงิน เพื่อให้ผู้ใช้สามารถดำเนินการงานต่อไปนี้ได้</span><span class="sxs-lookup"><span data-stu-id="35eb2-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="35eb2-111">ตั้งค่าคอนฟิกตัวเชื่อมต่อทางการเงิน ซึ่งเป็นอุปกรณ์หรือบริการทางการเงินที่ใช้เพื่อวัตถุประสงค์ทางการลงทะเบียนทางการเงิน เช่นเดียวกับการบันทึก ลายเซ็นดิจิทัล และการส่งได้รับการรักษาความปลอดภัยของข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="35eb2-112">ตั้งค่าคอนฟิกผู้ให้บริการเอกสาร ซึ่งกำหนดวิธีการแสดงผลและอัลกอริทึมของการสร้างเอกสารทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="35eb2-113">ตั้งค่าคอนฟิกกระบวนการลงทะเบียนทางการเงิน ซึ่งจะกำหนดลำดับของขั้นตอนและกลุ่มของตัวเชื่อมต่อที่ใช้ในแต่ละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="35eb2-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="35eb2-114">กำหนดกระบวนการลงทะเบียนทางการเงินไปยังโพรไฟล์ฟังก์ชันของ POS</span><span class="sxs-lookup"><span data-stu-id="35eb2-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="35eb2-115">กำหนดโพรไฟล์ทางเทคนิคของตัวเชื่อมต่อ ให้กับโพรไฟล์ฮาร์ดแวร์ (สำหรับตัวเชื่อมต่อทางการเงินแบบเฉพาะ) หรือไปยังโพรไฟล์ฟังก์ชัน POS (สำหรับชนิดตัวเชื่อมต่อทางการเงินอื่น) อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35eb2-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="35eb2-116">ขั้นตอนการดำเนินการรวมทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="35eb2-117">สถานการณ์จำลองต่อไปนี้แสดงขั้นตอนการดำเนินการรวมทางการเงินทั่วไป</span><span class="sxs-lookup"><span data-stu-id="35eb2-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="35eb2-118">การเริ่มต้นของกระบวนการลงทะเบียนทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="35eb2-119">หลังจากการดำเนินการบางอย่างที่จำเป็นต้องมีการลงทะเบียนทางการเงิน เช่น หลังจากมีการสรุปธุรกรรมขายปลีก กระบวนการลงทะเบียนทางการเงินจะเชื่อมโยงกับโพรไฟล์ฟังก์ชันของ POS ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="35eb2-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="35eb2-120">ค้นหาตัวเชื่อมต่อทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="35eb2-121">สำหรับขั้นตอนการลงทะเบียนทางการเงินแต่ละขั้นที่รวมอยู่ในกระบวนการลงทะเบียนทางการเงิน ระบบจะจับคู่กับรายการของตัวเชื่อมต่อทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="35eb2-122">ตัวเชื่อมต่อเหล่านี้มีโพรไฟล์การทำงานที่รวมอยู่ในกลุ่มตัวเชื่อมต่อที่ระบุ พร้อมกับรายการของตัวเชื่อมต่อที่มีโพรไฟล์ทางเทคนิคที่เชื่อมโยงกับโพรไฟล์ฮาร์ดแวร์ปัจจุบัน (สำหรับชนิดของตัวเชื่อมต่อที่เท่ากับ **เฉพาะที่** เท่านั้น) หรือพร้อมกับโพรไฟล์ฟังก์ชัน POS ปัจจุบัน (สำหรับชนิดตัวเชื่อมต่ออื่นๆ)</span><span class="sxs-lookup"><span data-stu-id="35eb2-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="35eb2-123">ทำการรวมทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="35eb2-124">ระบบปฏิบัติการดำเนินการทั้งหมดที่จำเป็น ซึ่งกำหนดโดยแอสเซมบลีที่เชื่อมโยงกับตัวเชื่อมต่อการค้นหา</span><span class="sxs-lookup"><span data-stu-id="35eb2-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="35eb2-125">ซึ่งจะกระทำโดยสอดคล้องกับการตั้งค่าของโพรไฟล์การทำงานและโพรไฟล์ทางเทคนิคที่พบในขั้นตอนก่อนหน้านี้สำหรับตัวเชื่อมต่อนี้</span><span class="sxs-lookup"><span data-stu-id="35eb2-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="35eb2-126">การตั้งค่าที่จำเป็นก่อนที่จะใช้การรวมทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="35eb2-127">ก่อนที่จะใช้ฟังก์ชันการรวมทางการเงิน คุณควรกำหนดการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="35eb2-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="35eb2-128">กำหนดลำดับหมายเลขบนหน้า **พารามิเตอร์การขายปลีก** สำหรับหมายเลขโพรไฟล์ฟังก์ชันทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="35eb2-129">กำหนดลำดับหมายเลขบนหน้า **พารามิเตอร์ที่ใช้ร่วมกันของ Retail** สำหรับการอ้างอิงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="35eb2-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="35eb2-130">หมายเลขโพรไฟล์เทคนิคทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="35eb2-131">หมายเลขกลุ่มของตัวเชื่อมต่อทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="35eb2-132">หมายเลขกระบวนการการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="35eb2-132">Registration process number</span></span>

- <span data-ttu-id="35eb2-133">สร้าง **ตัวเชื่อมต่อทางการเงิน** ใน **Retail > การตั้งค่าช่องทาง > การรวมทางการเงิน > ตัวเชื่อมต่อทางการเงิน** สำหรับแต่ละอุปกรณ์หรือบริการที่คุณวางแผนจะใช้สำหรับวัตถุประสงค์การรวมทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="35eb2-134">สร้าง **ตัวให้บริการเอกสารทางการเงิน** ใน **Retail > การตั้งค่าช่องทาง > การรวมทางการเงิน > ผู้ให้บริการเอกสารทางการเงิน** สำหรับตัวเชื่อมต่อทางการเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="35eb2-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="35eb2-135">การแม็ปข้อมูลจะถือเป็นส่วนหนึ่งของตัวให้บริการเอกสารทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="35eb2-136">ในการตั้งค่าการแม็ปข้อมูลที่แตกต่างกันสำหรับตัวเชื่อมต่อเดียวกัน (เช่น ข้อบังคับเฉพาะรัฐ) คุณควรสร้างผู้ให้บริการเอกสารทางการเงินที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="35eb2-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="35eb2-137">สร้าง **โพรไฟล์การทำงานของตัวเชื่อมต่อ** ใน **Retail > การตั้งค่าช่องทาง > การรวมทางการเงิน > โพรไฟล์การทำงานของตัวเชื่อมต่อ** สำหรับผู้ให้บริการเอกสารทางการเงินแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="35eb2-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="35eb2-138">เลือกชื่อตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="35eb2-138">Select a connector name.</span></span>
  - <span data-ttu-id="35eb2-139">เลือกผู้ให้บริการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="35eb2-139">Select a document provider.</span></span>
  - <span data-ttu-id="35eb2-140">ระบุการตั้งค่าอัตรา VAT บนแท็บ **การตั้งค่าบริการ**</span><span class="sxs-lookup"><span data-stu-id="35eb2-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="35eb2-141">ระบุการแม็ปรหัส VAT และการแม็ปชนิดของวิธีการชำระเงินบนแท็บ **การแม็ปข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="35eb2-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="35eb2-142">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="35eb2-142">Examples</span></span> 

  |  | <span data-ttu-id="35eb2-143">รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="35eb2-143">Format</span></span> | <span data-ttu-id="35eb2-144">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="35eb2-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="35eb2-145">การตั้งค่าอัตรา VAT</span><span class="sxs-lookup"><span data-stu-id="35eb2-145">VAT rates settings</span></span> | <span data-ttu-id="35eb2-146">ค่า: VATrate</span><span class="sxs-lookup"><span data-stu-id="35eb2-146">value : VATrate</span></span> | <span data-ttu-id="35eb2-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="35eb2-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="35eb2-148">การแม็ปรหัส VAT</span><span class="sxs-lookup"><span data-stu-id="35eb2-148">VAT codes mapping</span></span> | <span data-ttu-id="35eb2-149">VATcode : ค่า</span><span class="sxs-lookup"><span data-stu-id="35eb2-149">VATcode : value</span></span> | <span data-ttu-id="35eb2-150">vat20: 1, vat18: 2</span><span class="sxs-lookup"><span data-stu-id="35eb2-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="35eb2-151">การแม็ปชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-151">Tender types mapping</span></span> | <span data-ttu-id="35eb2-152">TenderTyp: ค่า</span><span class="sxs-lookup"><span data-stu-id="35eb2-152">TenderTyp : value</span></span> | <span data-ttu-id="35eb2-153">เงินสด: 1, บัตร : 2</span><span class="sxs-lookup"><span data-stu-id="35eb2-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="35eb2-154">สร้าง **กลุ่มตัวเชื่อมต่อทางการเงิน** ใน **Retail > การตั้งค่าช่องทาง > การรวมทางการเงิน > กลุ่มตัวเชื่อมต่อทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="35eb2-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="35eb2-155">กลุ่มตัวเชื่อมต่อคือ ชุดย่อยของโพรไฟล์การทำงานต่างๆ ที่เชื่อมโยงกับตัวเชื่อมต่อทางการเงินที่ทำหน้าที่เหมือนกัน และถูกใช้ในขั้นตอนเดียวกันภายในกระบวนการลงทะเบียนทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="35eb2-156">เพิ่มโพรไฟล์การทำงานไปยังกลุ่มของตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="35eb2-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="35eb2-157">คลิก **เพิ่ม** ในหน้า **โพรไฟล์การทำงาน** และเลือกหมายเลขโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="35eb2-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="35eb2-158">ถ้าคุณต้องการระงับการใช้โพรไฟล์การทำงาน ตั้งค่า **ปิดใช้งาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="35eb2-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="35eb2-159">การเปลี่ยนแปลงนี้มีผลต่อกลุ่มตัวเชื่อมต่อปัจจุบันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="35eb2-159">This change affects the current connector group only.</span></span> <span data-ttu-id="35eb2-160">คุณสามารถดำเนินต่อโดยใช้โพรไฟล์การทำงานเดียวกันในกลุ่มตัวเชื่อมต่ออื่นๆ</span><span class="sxs-lookup"><span data-stu-id="35eb2-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="35eb2-161">ภายในกลุ่มตัวเชื่อมต่อ ตัวเชื่อมต่อทางการเงินแต่ละรายการสามารถมีโพรไฟล์ฟังก์หนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="35eb2-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="35eb2-162">สร้าง **โพรไฟล์ทางเทคนิคของตัวเชื่อมต่อ** ใน **Retail > การตั้งค่าช่องทาง > การรวมทางการเงิน > โพรไฟล์ทางเทคนิคของตัวเชื่อมต่อ** สำหรับตัวเชื่อมต่อทางการเงินแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="35eb2-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="35eb2-163">เลือกชื่อตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="35eb2-163">Select a connector name.</span></span>
  - <span data-ttu-id="35eb2-164">เลือกชนิดของตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="35eb2-164">Select a connector type:</span></span> 
      - <span data-ttu-id="35eb2-165">**เฉพาะที่** - ตั้งค่าชนิดนี้สำหรับอุปกรณ์ทางกายภาพหรือแอพลิเคชันที่ติดตั้งบนเครื่องจักรเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="35eb2-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="35eb2-166">**ภายใน** - ตั้งค่าชนิดนี้สำหรับอุปกรณ์ทางการเงิน และบริการที่เชื่อมต่อกับเซิร์ฟเวอร์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="35eb2-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="35eb2-167">**ภายนอก** - สำหรับบริการทางการเงินภายนอก เช่น เว็บพอร์ทัลที่มีให้โดยหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="35eb2-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="35eb2-168">ระบุการตั้งค่าบนแท็บ **ตัวเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="35eb2-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="35eb2-169">รุ่นที่ปรับปรุงของการตั้งค่าคอนฟิกที่โหลดไว้ก่อนหน้า จะถูกโหลดสำหรับทั้งโพรไฟล์การทำงานและทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="35eb2-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="35eb2-170">ถ้าใช้ตัวเชื่อมต่อที่เหมาะสมหรือผู้ให้บริการเอกสารอยู่แล้ว คุณจะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="35eb2-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="35eb2-171">โดยค่าเริ่มต้น มีการจัดเก็บการเปลี่ยนแปลงทั้งหมดที่ทำไว้ด้วยตนเองในโพรไฟล์การทำงานและทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="35eb2-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="35eb2-172">เมื่อต้องการแทนที่โพรไฟล์เหล่านี้ด้วยชุดเริ่มต้นของพารามิเตอร์จากการตั้งค่าคอนฟิก คลิก **การอัพเดต** บนหน้า **โพรไฟล์ฟังก์ชันของตัวเชื่อมต่อ** และหน้า **โพรไฟล์ทางเทคนิคของตัวเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="35eb2-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="35eb2-173">สร้าง **กระบวนการลงทะเบียนทางการเงิน** ใน **Retail > การตั้งค่าช่องทาง > การรวมทางการเงิน > กระบวนการลงทะเบียนทางการเงิน** สำหรับกระบวนการแต่ละกระบวนการที่ไม่ซ้ำกันของการรวมทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35eb2-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="35eb2-174">กระบวนการลงทะเบียนจะถูกกำหนดโดยลำดับของขั้นตอนการลงทะเบียน และกลุ่มตัวเชื่อมต่อที่ใช้ในแต่ละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="35eb2-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="35eb2-175">เพิ่มขั้นตอนการลงทะเบียนไปยังกระบวนการ:</span><span class="sxs-lookup"><span data-stu-id="35eb2-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="35eb2-176">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="35eb2-176">Click **Add**.</span></span>
      - <span data-ttu-id="35eb2-177">เลือกชนิดตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="35eb2-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="35eb2-178">ฟิลด์นี้กำหนดที่ซึ่งระบบจะค้นหาในโพรไฟล์ทางเทคนิคสำหรับตัวเชื่อมต่อ ในโพรไฟล์ฮาร์ดแวร์สำหรับชนิดตัวเชื่อมต่อ **เฉพาะที่** หรือในโพรไฟล์ฟังก์ชันของ POS อย่างใดอย่างหนึ่ง สำหรับชนิดตัวเชื่อมต่อทางการเงินอื่น</span><span class="sxs-lookup"><span data-stu-id="35eb2-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="35eb2-179">เลือกกลุ่มตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="35eb2-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="35eb2-180">คลิก **ตรวจสอบ** เพื่อตรวจสอบความถูกต้องของโครงสร้างกระบวนการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="35eb2-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="35eb2-181">ขอแนะนำให้ทำการตรวจสอบในกรณีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="35eb2-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="35eb2-182">สำหรับกระบวนการลงทะเบียนใหม่ หลังจากตั้งค่าทั้งหมดเสร็จสมบูรณ์แล้ว ซึ่งรวมทั้งการผูกกับโพรไฟล์ฟังก์ชัน POS และโพรไฟล์ฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="35eb2-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="35eb2-183">หลังจากทำการปรับปรุงลงในกระบวนการลงทะเบียนที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="35eb2-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="35eb2-184">ผูกกระบวนการลงทะเบียนทางการเงินกับโพรไฟล์ฟังก์ชัน POS ใน **Retail > การตั้งค่าช่องทาง > การตั้งค่า POS > โพรไฟล์ POS > โพรไฟล์ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="35eb2-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="35eb2-185">คลิก **แก้ไข** และเลือก **หมายเลขกระบวนการ** ในแท็บ **กระบวนการลงทะเบียนทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="35eb2-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="35eb2-186">ผูกโพรไฟล์ทางเทคนิคของตัวเชื่อมต่อกับโพรไฟล์ฮาร์ดแวร์ใน **Retail > ช่องทางการตั้งค่า > การตั้งค่า POS > โพรไฟล์ POS > โพรไฟล์ฮาร์ดแวร์**</span><span class="sxs-lookup"><span data-stu-id="35eb2-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="35eb2-187">คลิก **แก้ไข** แล้ว คลิก **สร้าง** ในแท็บ **โพรไฟล์ทางเทคนิคทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="35eb2-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="35eb2-188">เลือกโพรไฟล์ทางเทคนิคของตัวเชื่อมต่อในฟิลด์ **หมายเลขของโพรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="35eb2-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="35eb2-189">คุณสามารถเพิ่มโพรไฟล์ทางเทคนิคหลายรายการไปยังโพรไฟล์ฮาร์ดแวร์ได้</span><span class="sxs-lookup"><span data-stu-id="35eb2-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="35eb2-190">อย่างไรก็ตาม รายการนี้ไม่ได้รับการสนับสนุน ถ้าโพรไฟล์ฮาร์ดแวร์มีจุดคาบเกี่ยวมากกว่าหนึ่งแห่งกับกลุ่มตัวเชื่อมต่อใดๆ</span><span class="sxs-lookup"><span data-stu-id="35eb2-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="35eb2-191">เพื่อหลีกเลี่ยงการตั้งค่าที่ไม่ถูกต้อง ขอแนะนำให้คุณตรวจสอบกระบวนการลงทะเบียน หลังจากการอัพเดตโพรไฟล์ฮาร์ดแวร์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="35eb2-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

