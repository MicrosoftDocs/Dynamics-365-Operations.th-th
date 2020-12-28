---
title: การประเมินเงื่อนไข
description: หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตการประเมินเงื่อนไขและการลงทะเบียนในสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 774c788959c5ebea69b4d22c886ac673f50b97f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438592"
---
# <a name="condition-assessment"></a><span data-ttu-id="5f044-103">การประเมินเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5f044-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5f044-104">หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตการประเมินเงื่อนไขและการลงทะเบียนในสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5f044-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="5f044-105">การประเมินเงื่อนไขจะดำเนินการตามช่วงเวลาปกติ และวัตถุประสงค์หลักคือการสร้างและรักษาข้อมูลเงื่อนไขในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5f044-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="5f044-106">ซึ่งเห็นได้จากมุมมองการบำรุงรักษาเชิงป้องกัน สิ่งสำคัญคือต้องตรวจสอบข้อมูลสำคัญ เช่น เงื่อนไขปัจจุบัน และช่วงชีวิตที่เหลืออยู่</span><span class="sxs-lookup"><span data-stu-id="5f044-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="5f044-107">นอกจากนี้ ถ้าคุณดำเนินการประเมินเงื่อนไขในช่วงเวลาปกติ คุณจะสามารถตรวจสอบและเปรียบเทียบเงื่อนไขบนเครื่องจักรในโรงงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="5f044-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="5f044-108">การประเมินเงื่อนไขสามารถใช้ในการวัดและตรวจสอบเงื่อนไขต่างๆ บนอุปกรณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5f044-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="5f044-109">ตัวอย่าง: คุณสามารถวัดแรงสั่นสะเทือนบนเครื่องจักรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="5f044-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="5f044-110">หลังจากที่คุณได้ลงทะเบียนการวัดค่าการสั่นสะเทือนในการจัดการสินทรัพย์ในอุปกรณ์ประเภทต่างๆแล้ว คุณจะสามารถค้นหาการประเมินที่ลงทะเบียนล่าสุดและสามารถดูการวัดการสั่นสะเทือนได้</span><span class="sxs-lookup"><span data-stu-id="5f044-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="5f044-111">การประเมินเงื่อนไขถูกสร้างขึ้นในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5f044-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="5f044-112">คุณตั้งค่าเท็มเพลตการประเมินเงื่อนไขบนชนิดสินทรัพย์ ก่อนที่คุณจะดำเนินการกระบวนงานการประเมินเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5f044-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="5f044-113">เหตุผลในการใช้เท็มเพลตสำหรับการประเมินเงื่อนไขคือ เพื่อหลีกเลี่ยงการเปลี่ยนแปลงของข้อมูลเงื่อนไขในสินทรัพย์ที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="5f044-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="5f044-114">ลำดับสำหรับการตั้งค่าและการใช้การประเมินเงื่อนไขในการจัดการสินทรัพย์คือ: ก่อนอื่นคุณตั้งค่าเท็มเพลตการประเมินเงื่อนไขที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="5f044-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="5f044-115">ถัดไป คุณเชื่อมโยงเท็มเพลตกับชนิดสินทรัพย์ในฟอร์ม **ชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5f044-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="5f044-116">สุดท้าย คุณสามารถสร้างการลงทะเบียนการประเมินเงื่อนไขในสินทรัพย์ในฟอร์ม **สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5f044-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="5f044-117">สร้างเท็มเพลตการประเมินเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5f044-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="5f044-118">เลือก **การจัดการสินทรัพย์** > **การตั้งค่า** > **ชนิดสินทรัพย์** > **การประเมินเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="5f044-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="5f044-119">เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="5f044-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="5f044-120">แทรกและรหัสสำหรับเท็มเพลตในฟิลด์ **เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="5f044-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="5f044-121">แทรกชื่อสำหรับเท็มเพลตในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="5f044-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="5f044-122">บน FastFab **รายการการประเมินเงื่อนไข** เพิ่มรายการที่จำเป็นสำหรับการประเมินเงื่อนไข ซึ่งรวมถึงการเลือกชนิดเงื่อนไขและหน่วยการวัดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="5f044-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="5f044-123">บน FastTab **ชนิดสินทรัพย์** ให้เพิ่มชนิดสินทรัพย์ที่ควรใช้เท็มเพลตการประเมินเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5f044-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="5f044-124">ในฟิลด์ **รายการ** และ **ชนิดสินทรัพย์** ในกลุ่ม **รายละเอียด** ที่ด้านบนของหน้าจอ คุณจะเห็นจำนวนของรายการการประเมินและชนิดสินทรัพย์ที่เกี่ยวข้องกับเท็มเพลตการประเมินเงื่อนไขที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f044-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="5f044-125">สร้างการลงทะเบียนการประเมินเงื่อนไขในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5f044-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="5f044-126">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5f044-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="5f044-127">ในรายการ เลือกสินทรัพย์ที่คุณต้องการสร้างการลงทะเบียนการประเมินเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5f044-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="5f044-128">ในแท็บ **ทั่วไป** คลิก **การประเมินเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="5f044-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="5f044-129">คลิก **สร้าง** เพื่อสร้างการลงทะเบียนใหม่</span><span class="sxs-lookup"><span data-stu-id="5f044-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="5f044-130">เลือกวันที่สำหรับการประเมินเงื่อนไขในฟิลด์ **วันที่**</span><span class="sxs-lookup"><span data-stu-id="5f044-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="5f044-131">เลือกชื่อของผู้ปฏิบัติงานที่ดำเนินการลงทะเบียนการประเมินในฟิลด์ **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="5f044-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="5f044-132">ในฟิลด์ **รายการ** คุณจะเห็นจำนวนของรายการการประเมินที่ตั้งค่าไว้ในการประเมินเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5f044-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="5f044-133">เลือกเท็มเพลตสำหรับการประเมินเงื่อนไขในฟิลด์ **เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="5f044-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="5f044-134">ชื่อของเท็มเพลตจะถูกแทรกโดยอัตโนมัติในฟิลด์ **ชื่อ** และรายการการลงทะเบียนที่เกี่ยวข้องจะถูกแทรกบน FastTab **รายการการประเมินเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="5f044-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="5f044-135">คุณสามารถแทรกบันทึกย่อที่เกี่ยวข้องกับการประเมินเงื่อนไขที่เลือกได้บน FastTab **บันทึกย่อ**</span><span class="sxs-lookup"><span data-stu-id="5f044-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="5f044-136">สำหรับรายการการประเมินเงื่อนไขแต่ละรายการ ให้แทรกข้อมูลการวัดในฟิลด์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="5f044-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="5f044-137">คุณสามารถแทรกข้อคิดเห็นที่เกี่ยวกับรายการการลงทะเบียนที่เลือกได้ใน FastTab **รายการการประเมินเงื่อนไข** > ฟิลด์ **ข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="5f044-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="5f044-138">ถ้าคุณเพิ่มข้อคิดเห็นบนรายการ จะมีการเลือกกล่องกาเครื่องหมาย **ข้อคิดเห็น** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5f044-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="5f044-139">หลังจากที่คุณได้ทำการลงทะเบียนการประเมินเงื่อนไขในสินทรัพย์แล้ว คุณสามารถพิมพ์รายงานการประเมินเงื่อนไขได้</span><span class="sxs-lookup"><span data-stu-id="5f044-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="5f044-140">นอกจากนี้ คุณยังสามารถลงทะเบียนการประเมินเงื่อนไขได้ในใบสั่งงาน (ปุ่ม **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** > **การประเมินเงื่อนไข**)</span><span class="sxs-lookup"><span data-stu-id="5f044-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
