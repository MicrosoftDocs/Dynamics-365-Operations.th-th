---
title: แก้ไขปัญหาระหว่างการตั้งค่าเริ่มแรก
description: หัวข้อนี้จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกิดขึ้นในระหว่างการตั้งค่าเริ่มต้นของการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6ff9a304de8a94b86e6866d6d2cb65fbfdfb02f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561189"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="0fcf7-103">แก้ไขปัญหาระหว่างการตั้งค่าเริ่มแรก</span><span class="sxs-lookup"><span data-stu-id="0fcf7-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0fcf7-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="0fcf7-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0fcf7-105">กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่อาจเกิดขึ้นในระหว่างการตั้งค่าเริ่มต้นของการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="0fcf7-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0fcf7-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="0fcf7-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0fcf7-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0fcf7-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="0fcf7-108">คุณไม่สามารถเชื่อมโยงแอป Finance and Operations กับ Dataverse ได้</span><span class="sxs-lookup"><span data-stu-id="0fcf7-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="0fcf7-109">**บทบาทที่จำเป็นในการตั้งค่าการรวมแบบสองทิศทาง:** ผู้ดูแลระบบในแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="0fcf7-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="0fcf7-110">ข้อผิดพลาดบนหน้า **ลิงค์การตั้งค่าไปยัง Dataverse** โดยปกติจะเกิดจากปัญหาการตั้งค่าที่ไม่สมบูรณ์หรือปัญหาของสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="0fcf7-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="0fcf7-111">ตรวจสอบให้แน่ใจว่าผ่านการตรวจสอบความสมบูรณ์ทั้งหมดบนหน้า **ลิงค์การตั้งค่าไปยัง Dataverse** ดังแสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0fcf7-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="0fcf7-112">คุณไม่สามารถเชื่อมโยงการรวมแบบสองทิศทางได้จนกว่าจะผ่านการตรวจสอบความสมบูรณ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0fcf7-112">You can't link dual-write unless the whole health check passes.</span></span>

![การตรวจสอบความสมบูรณ์ที่ประสบความสำเร็จ](media/health_check.png)

<span data-ttu-id="0fcf7-114">คุณต้องมีข้อมูลประจำตัวของผู้ดูแลระบบผู้เช่า Azure AD เพื่อเชื่อมโยงสภาพแวดล้อม Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="0fcf7-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="0fcf7-115">หลังจากที่คุณเชื่อมโยงสภาพแวดล้อมแล้ว ผู้ใช้สามารถลงชื่อเข้าใช้ได้โดยใช้ข้อมูลประจำตัวของบัญชีผู้ใช้และปรับปรุงแม็ปตารางที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0fcf7-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="0fcf7-116">ข้อผิดพลาดเมื่อคุณเปิดลิงค์ไปยังหน้า Dataverse</span><span class="sxs-lookup"><span data-stu-id="0fcf7-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="0fcf7-117">**ข้อมูลประจำตัวที่จำเป็นในแก้ปัญหา:** ผู้ดูแลระบบผู้เช่า Azure AD</span><span class="sxs-lookup"><span data-stu-id="0fcf7-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="0fcf7-118">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณเปิด **ลิงค์ไปยังหน้า Dataverse** ในแอป Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="0fcf7-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="0fcf7-119">*รหัสสถานะการตอบสนองไม่บ่งชี้ความสำเร็จ: 404 (ไม่พบ)*</span><span class="sxs-lookup"><span data-stu-id="0fcf7-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="0fcf7-120">ข้อผิดพลาดนี้จะเกิดขึ้นเมื่อขั้นตอนความยินยอมยังไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0fcf7-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="0fcf7-121">เมื่อต้องการตรวจสอบว่าขั้นตอนความยินยอมเสร็จสมบูรณ์หรือไม่ให้ ลงชื่อเข้าใช้ใน portal.Azure.com โดยใช้บัญชีผู้ดูแลระบบผู้เช่า Azure AD และดูว่าแอพของบุคคลที่สามที่มีรหัส **33976c19-1db5-4c02-810e-c243db79efde** ปรากฏขึ้นในรายการ **แอพลิเคชันองค์กร** ของ Azure AD หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0fcf7-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="0fcf7-122">ถ้าไม่ใช่ คุณต้องให้ความยินยอมจากแอป</span><span class="sxs-lookup"><span data-stu-id="0fcf7-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="0fcf7-123">เพื่อให้ความยินยอมจากแอป ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0fcf7-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="0fcf7-124">เปิด URL ต่อไปนี้โดยใช้ข้อมูลประจำตัวของผู้ดูแลระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="0fcf7-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="0fcf7-125">คุณควรได้รับพร้อมท์สำหรับความยินยอม</span><span class="sxs-lookup"><span data-stu-id="0fcf7-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="0fcf7-126">เลือก **ยอมรับ** เพื่อระบุว่าคุณกำลังให้ความยินยอมในการติดตั้งแอปที่มีรหัส **33976c19-1db5-4c02-810e-c243db79efde** ในผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="0fcf7-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="0fcf7-127">ต้องใช้แอปนี้ในการเชื่อมโยงแอป Dataverse และแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0fcf7-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="0fcf7-128">ถ้าคุณมีปัญหาในขั้นตอนนี้ ให้เปิดเบราว์เซอร์ของคุณในโหมดที่ไม่ระบุตัวตน (ใน Google Chrome) หรือโหมด InPrivate (ใน Microsoft Edge)</span><span class="sxs-lookup"><span data-stu-id="0fcf7-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="0fcf7-129">ตรวจสอบว่ามีการตั้งค่าข้อมูลของบริษัทและทีมงานการรวมแบบสองทิศทางไว้อย่างถูกต้องในระหว่างการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="0fcf7-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="0fcf7-130">เพื่อให้แน่ใจว่าการรวมแบบสองทิศทางทำงานได้อย่างถูกต้อง บริษัทที่คุณเลือกในระหว่างการตั้งค่าคอนฟิกจะถูกสร้างขึ้นในสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="0fcf7-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="0fcf7-131">โดยค่าเริ่มต้น บริษัทเหล่านี้เป็นแบบอ่านอย่างเดียว และมีการตั้งค่าคุณสมบัติ **IsDualWriteEnable** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="0fcf7-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="0fcf7-132">นอกจากนี้ เจ้าของหน่วยธุรกิจและทีมงานที่เป็นเจ้าของเริ่มต้นจะถูกสร้างขึ้นและรวมถึงชื่อบริษัท</span><span class="sxs-lookup"><span data-stu-id="0fcf7-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="0fcf7-133">ก่อนที่คุณจะเปิดใช้งานแผนที่ ให้ตรวจสอบว่ามีการระบุเจ้าของทีมงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0fcf7-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="0fcf7-134">เมื่อต้องการค้นหาตาราง **บริษัท (CDM\_บริษัท)** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0fcf7-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="0fcf7-135">ในแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้เลือกตัวกรองในมุมด้านขวาบน</span><span class="sxs-lookup"><span data-stu-id="0fcf7-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="0fcf7-136">ในรายการแบบหล่นลง เลือก **บริษัท**</span><span class="sxs-lookup"><span data-stu-id="0fcf7-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="0fcf7-137">เลือก **รัน** เพื่อดูผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0fcf7-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="0fcf7-138">เลือกบริษัทที่ถูกเชื่อมโยง เมื่อคุณตั้งค่าคอนฟิกการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="0fcf7-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="0fcf7-139">ตรวจสอบว่าคอลัมน์ **ทีมงานที่เป็นเจ้าของเริ่มต้น** มีค่า</span><span class="sxs-lookup"><span data-stu-id="0fcf7-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="0fcf7-140">ในภาพประกอบต่อไปนี้ จะมีการตั้งค่าคอลัมน์ **ทีมงานที่เป็นเจ้าของเริ่มต้น** เป็น **การรวมแบบสองทิศทาง USMF**</span><span class="sxs-lookup"><span data-stu-id="0fcf7-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![การตรวจสอบทีมงานที่เป็นเจ้าของเริ่มต้น](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="0fcf7-142">ค้นหาขีดจำกัดของจำนวนตารางทางกฎหมายหรือบริษัทที่สามารถเชื่อมโยงสำหรับการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="0fcf7-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="0fcf7-143">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามที่จะเปิดใช้งานแผนที่:</span><span class="sxs-lookup"><span data-stu-id="0fcf7-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="0fcf7-144">*ความล้มเหลวในการรวมแบบสองทิศทาง - การลงทะเบียนปลั๊กอินล้มเหลว: \[ไม่สามารถเรียกดูแผนผังพาร์ทิชันสำหรับโครงการ DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea ข้อผิดพลาดเกินกว่าพาร์ติชันสูงสุดที่อนุญาตให้สำหรับการแม็ป DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea\] เกิดข้อผิดพลาดอย่างน้อยหนึ่งรายการ*</span><span class="sxs-lookup"><span data-stu-id="0fcf7-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="0fcf7-145">ขีดจำกัดปัจจุบันเมื่อคุณเชื่อมโยงสภาพแวดล้อมคือนตารางทางกฎหมายประมาณ 40 ราย</span><span class="sxs-lookup"><span data-stu-id="0fcf7-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="0fcf7-146">ข้อผิดพลาดนี้จะเกิดขึ้น ถ้าคุณพยายามเปิดใช้งานแผนที่ และมีการเชื่อมโยงนตารางทางกฎหมายมากกว่า 40 รายระหว่างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="0fcf7-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]