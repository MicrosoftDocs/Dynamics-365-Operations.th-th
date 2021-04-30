---
title: การรายงานภาษีหัก ณ ที่จ่ายสำหรับอียิปต์
description: หัวข้อนี้อธิบายวิธีการกำหนดค่าคอนฟิกและสร้างการรายงานภาษีหัก ณ ที่จ่ายสำหรับอียิปต์
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e0d13a2de9acaa8b1c896e130b4dabb222e45dcb
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881433"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="3d64b-103">การรายงานภาษีหัก ณ ที่จ่ายสำหรับอียิปต์ (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="3d64b-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="3d64b-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="3d64b-104">Overview</span></span>
<span data-ttu-id="3d64b-105">หัวข้อนี้อธิบายวิธีการตั้งค่าและสร้างการรายงานภาษีหัก ณ ที่จ่าย และแบบฟอร์มการรายงานภาษีหัก ณ ที่จ่าย แบบฟอร์ม 41 และ 11 ของนิติบุคคลในอียิปต์</span><span class="sxs-lookup"><span data-stu-id="3d64b-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="3d64b-106">นิติบุคคลของอียิปต์ทั้งหมดต้องจัดเตรียมแบบฟอร์ม 41 ซึ่งจะสรุปภาษีทั้งหมดที่เก็บจากซัพพลายเออร์และผู้ให้บริการในพื้นที่</span><span class="sxs-lookup"><span data-stu-id="3d64b-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="3d64b-107">นอกจากแบบฟอร์ม 41 แล้ว ต้องสร้างแบบฟอร์ม 11 เพื่อดูรายละเอียดของภาษีที่จัดเก็บทั้งหมดจากผู้ให้บริการต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="3d64b-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="3d64b-108">รายงาน **การรายงานภาษีหัก ณ ที่จ่าย** ใน Dynamics 365 Finance จะรวมถึงรายงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3d64b-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="3d64b-109">แบบฟอร์มการรายงานภาษีหมายเลข</span><span class="sxs-lookup"><span data-stu-id="3d64b-109">Declaration form No.</span></span> <span data-ttu-id="3d64b-110">41</span><span class="sxs-lookup"><span data-stu-id="3d64b-110">41</span></span>
- <span data-ttu-id="3d64b-111">แบบฟอร์มการรายงานภาษีหมายเลข</span><span class="sxs-lookup"><span data-stu-id="3d64b-111">Declaration form No.</span></span> <span data-ttu-id="3d64b-112">11</span><span class="sxs-lookup"><span data-stu-id="3d64b-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="3d64b-113">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="3d64b-113">Prerequisites</span></span>
<span data-ttu-id="3d64b-114">ที่อยู่หลักของนิติบุคคลต้องอยู่ในอียิปต์</span><span class="sxs-lookup"><span data-stu-id="3d64b-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="3d64b-115">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ต้องเปิดใช้งานคุณลักษณะต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3d64b-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="3d64b-116">**ภาษีหัก ณ ที่จ่ายทั่วโลก**</span><span class="sxs-lookup"><span data-stu-id="3d64b-116">**Global withholding tax**</span></span>

<span data-ttu-id="3d64b-117">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะ ดูที่ [ภาพรวมของการจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3d64b-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="3d64b-118">ไปที่ **ภาษี** > **การตั้งค่า** > **พารามิเตอร์** > **พารามิเตอร์บัญชีแยกประเภททั่วไป**, และบนแท็บ **ภาษีหัก ณ ที่จ่าย** ให้ตั้งค่าตัวเลือก **Enable glเปิดใช้งานภาษีหัก ณ ที่จ่ายแบบสากล** เป็น **ใช่** </span><span class="sxs-lookup"><span data-stu-id="3d64b-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="3d64b-119">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ให้นําเข้ารูปแบบการรายงานทางอิเล็กทรอนิกส์ต่อไปนี้จากที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="3d64b-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="3d64b-120">Excel การรายงาน WHT (EG)</span><span class="sxs-lookup"><span data-stu-id="3d64b-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d64b-121">รูปแบบข้างต้นจะขึ้นอยู่กับ **แบบจำลองการรายงานภาษี** และใช้ **การทำแผนที่แบบจำลองการรายงานภาษี**</span><span class="sxs-lookup"><span data-stu-id="3d64b-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="3d64b-122">การกำหนดค่าเพิ่มเติมนี้จะถูกนําเข้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3d64b-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="3d64b-123">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีนําเข้าการกำหนดค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ ดูได้ที่ [ดาวน์โหลดการกำหนดค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์จาก Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)</span><span class="sxs-lookup"><span data-stu-id="3d64b-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="3d64b-124">ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="3d64b-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="3d64b-125">การใช้งานแบบฟอร์ม WHT declaration สำหรับอียิปต์จะขึ้นอยู่กับการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="3d64b-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="3d64b-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความสามารถและแนวคิดของการรายงานที่สามารถตั้งค่าคอนฟิกได้ โปรดดูที่ [การรายงานทางอิเล็กทรอนิกส์](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="3d64b-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="3d64b-127">สำหรับสภาพแวดล้อมการผลิตและการทดสอบการยอมรับของผู้ใช้ (UAT) ให้ปฏิบัติตามคําแนะนําในหัวข้อ [ดาวน์โหลดการกำหนดค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์จาก Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)</span><span class="sxs-lookup"><span data-stu-id="3d64b-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="3d64b-128">หากต้องการสร้างการรายงานภาษีหัก ณ ที่จ่ายในนิติบุคคลอียิปต์ คุณต้องอัพโหลดการกำหนดค่าคอนฟิกต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3d64b-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="3d64b-129">Tax declaration model.version.82.xml หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="3d64b-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="3d64b-130">Tax declaration model mapping.version.82.133.xml หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="3d64b-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="3d64b-131">Excel การรายงาน WHT (EG).version.82.21 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="3d64b-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="3d64b-132">หลังจากที่คุณดาวน์โหลดการกำหนดค่าคอนฟิก ER จาก Lifecycle Services (LCS) หรือที่เก็บส่วนกลางเสร็จแล้ว ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3d64b-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="3d64b-133">ไปยังพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** และเลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="3d64b-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="3d64b-134">บนหน้า **การกำหนดค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ เลือก **การแลกเปลี่ยน > โหลดจากไฟล์ XML**   </span><span class="sxs-lookup"><span data-stu-id="3d64b-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="3d64b-135">อัพโหลดไฟล์ทั้งหมดตามลำดับที่แสดงในสัญลักษณ์แสดงหัวข้อย่อยก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="3d64b-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="3d64b-136">หลังจากอัพโหลดการกำหนดค่าคอนฟิกทั้งหมดแล้ว แผนภูมิการกำหนดค่าคอนฟิกควรแสดงใน Finance</span><span class="sxs-lookup"><span data-stu-id="3d64b-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="3d64b-137">ตั้งค่าพารามิเตอร์เฉพาะแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3d64b-137">Set up application-specific parameters</span></span>

<span data-ttu-id="3d64b-138">ตัวเลือกพารามิเตอร์เฉพาะแอพพลิเคชันช่วยให้ผู้ใช้สามารถกำหนดเกณฑ์การการจัดประเภทและคํานวณธุรกรรมภาษีในแต่ละบรรทัดของรายงานที่สร้างขึ้น ได้ โดยขึ้นอยู่กับการกำหนดค่าคอนฟิกของ **กลุ่มรายการภาษีหัก ณ ที่จ่าย** หรือเกณฑ์อื่นๆ ที่กําหนดไว้ในคำจำกัดความของการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3d64b-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="3d64b-139">แบบฟอร์มการรายงานภาษีหัก ณ ที่จ่าย 41 รวมคอลัมน์เฉพาะที่ต้องจัดประเภทธุรกรรมภาษีหัก ณ ที่จ่าย ตามการจัดประเภทหน่วยงานจัดเก็บภาษีที่มีชื่อว่า **ชนิดของรหัสส่วนลด**</span><span class="sxs-lookup"><span data-stu-id="3d64b-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="3d64b-140">แทนที่จะรวมการจัดประเภทใหม่เหล่านี้เป็นข้อมูลรายการใหม่เมื่อมีการลงรายการบัญชีธุรกรรม การจัดประเภทจะถูกกําหนดตามการค้นหาต่างๆ ที่แนะนำใน **การกำหนดค่าคอนฟิก** > **ให้ตั้งค่าพารามิเตอร์เฉพาะแอพลิเคชัน** > **การตั้งค่า** เพื่อให้ตรงกับความต้องการของรายงานภาษีหัก ณ ที่จ่ายของอียิปต์</span><span class="sxs-lookup"><span data-stu-id="3d64b-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="3d64b-141">การกำหนดค่าคอนฟิกต่อไปนี้จะถูกใช้ในการจัดประเภทธุรกรรมในแบบฟอร์มการรายงานภาษีหัก ณ ที่จ่าย 41</span><span class="sxs-lookup"><span data-stu-id="3d64b-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="3d64b-142">**DiscountTaxTypeLookup**-> คอลัมน์หมายเลข 18</span><span class="sxs-lookup"><span data-stu-id="3d64b-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="3d64b-143">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าการค้นหาต่างๆ กันที่ใช้ในการสร้างรายงาน WHT declaration และ รายงานสมุดบัญชีที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3d64b-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="3d64b-144">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือก **การกำหนดค่าคอนฟิก** > **การตั้งค่า** เพื่อตั้งค่ากฎเพื่อระบุวิธีการจัดประเภทธุรกรรมภาษีในรายงาน WHT declaration</span><span class="sxs-lookup"><span data-stu-id="3d64b-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="3d64b-145">เลือกรุ่นปัจจุบัน และบน FastTab **Lookups** เลือกชื่อการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3d64b-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="3d64b-146">ตัวอย่างเช่น **DiscountTaxTypeLookup**</span><span class="sxs-lookup"><span data-stu-id="3d64b-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="3d64b-147">การค้นหานี้จะระบุรายการประเภทส่วนลดที่หน่วยงานจัดเก็บภาษีต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3d64b-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="3d64b-148">บน FastTab **เงื่อนไข** ให้เลือก **เพิ่ม** และในบรรทัดใหม่ ในคอลัมน์ **ผลลัพธ์การค้นหา** ให้เลือกบรรทัดที่เกี่ยวข้องซึ่งแสดงถึงการจำแนกประเภทใน **คอลัมน์ 18**</span><span class="sxs-lookup"><span data-stu-id="3d64b-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="3d64b-149">ในคอลัมน์ **กลุ่มรายการภาษีหัก ณ ที่จ่าย** ให้เลือกรหัสที่เกี่ยวข้องที่ใช้ในการระบุประเภท</span><span class="sxs-lookup"><span data-stu-id="3d64b-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="3d64b-150">ตัวอย่างเช่น **ส่วนลดที่อนุญาต**</span><span class="sxs-lookup"><span data-stu-id="3d64b-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="3d64b-151">ทําซ้ำขั้นตอนที่ 3 และ 4 สำหรับการค้นหาที่พร้อมใช้งานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3d64b-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="3d64b-152">เลือก **เพิ่ม** อีกครั้งเพื่อรวมบรรทัดเรกคอร์ดสุดท้าย และในคอลัมน์ **ผลลัพธ์การค้นหา** ให้เลือก **ไม่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="3d64b-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="3d64b-153">ในคอลัมน์ที่เหลือ ให้เลือก **ไม่เว้นว่าง**</span><span class="sxs-lookup"><span data-stu-id="3d64b-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="3d64b-154">ตั้งค่าพารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="3d64b-154">Set up General ledger parameters</span></span>

<span data-ttu-id="3d64b-155">ในการสร้างรายงานแบบฟอร์มการรายงานภาษี WHT ใน Microsoft Excel ให้กําหนดรูปแบบ ER บนหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="3d64b-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="3d64b-156">ไปที่ **ภาษี** > **การตั้งค่า** > **พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="3d64b-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="3d64b-157">บนแท็บ **ภาษีหัก ณ ที่จ่าย** ในเขตข้อมูล **การแม็ปรูปแบบการรายงาน WHT** เลือก **Excel การรายงาน WHT (EG)**</span><span class="sxs-lookup"><span data-stu-id="3d64b-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="3d64b-158">หากคุณปล่อยเขตข้อมูลนี้ว่างไว้ รายงานภาษีขายมาตรฐานจะถูกสร้างในรูปแบบ SSRS</span><span class="sxs-lookup"><span data-stu-id="3d64b-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![แบบฟอร์มการรายงานภาษี](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="3d64b-160">สร้างแบบฟอร์มการรายงานภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="3d64b-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="3d64b-161">ขั้นตอนการจัดเตรียมและยื่นแบบฟอร์มการรายงานภาษีหัก ณ ที่จ่ายในรอบระยะเวลาที่ระบุ ขึ้นอยู่กับธุรกรรมภาษีหัก ณ ที่จ่ายที่ลงรายการบัญชีระหว่างงานการหักภาษี ณ ที่จ่ายและลงรายการบัญชีงานภาษีการหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="3d64b-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="3d64b-162">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับภาษีหัก ณ ที่จ่ายสากล ดูได้ที่ [ภาษีหัก ณ ที่จ่ายสากล](../general-ledger/global-withholding-tax-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3d64b-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="3d64b-163">ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อสร้างรายงานภาษี</span><span class="sxs-lookup"><span data-stu-id="3d64b-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="3d64b-164">ไปที่ **ภาษี** > **การรายงาน** > **หัก ณ จ่าย** > \**การชำระภาษีหัก ณ ที่จ่าย*</span><span class="sxs-lookup"><span data-stu-id="3d64b-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="3d64b-165">เลือกรอบระยะเวลาการจ่ายเงินแล้วเลือกวันที่เริ่มต้นของรายงาน</span><span class="sxs-lookup"><span data-stu-id="3d64b-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="3d64b-166">ป้อนวันที่ทำธุรกรรมแล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3d64b-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="3d64b-167">ในกล่องโต้ตอบที่เปิดขึ้น ให้เลือกชนิดแบบฟอร์มอย่างน้อยหนึ่งประเภท **แบบฟอร์มหมายเลข 41** **แบบฟอร์มหมายเลข 11** หรือ **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="3d64b-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="3d64b-168">ถ้าคุณเลือก **ไม่มี** ระบบจะสร้างรายงานมาตรฐานเอง</span><span class="sxs-lookup"><span data-stu-id="3d64b-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="3d64b-169">เลือกภาษา</span><span class="sxs-lookup"><span data-stu-id="3d64b-169">Select the language.</span></span> <span data-ttu-id="3d64b-170">รายงานทั้งหมดมีการแปลอยู่ใน **en-us** และ **ar-eg**</span><span class="sxs-lookup"><span data-stu-id="3d64b-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="3d64b-171">ป้อนสาขาและชื่อของธนาคารที่จะป้อนจะทำการชำระภาษี</span><span class="sxs-lookup"><span data-stu-id="3d64b-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="3d64b-172">เลือกประเภทธุรกิจแล้วป้อนหมายเลขเช็คและหมายเลขเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3d64b-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="3d64b-173">ป้อนประเภทของนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="3d64b-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="3d64b-174">ป้อนชื่อของบุคคลที่ลงทะเบียนเพื่อกําหนดแบบฟอร์มและเลือก **ตกลง** เพื่อยืนยันการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="3d64b-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
