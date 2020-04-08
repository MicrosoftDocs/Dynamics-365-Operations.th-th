---
title: แก้ไขปัญหาเกี่ยวกับโมดูลการรวมแบบสองทิศทางในแอป Finance and Operations
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาด้วยโมดูลการรวมแบบสองทิศทางในแอป Finance and Operations
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172771"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="3cc2a-103">แก้ไขปัญหาเกี่ยวกับโมดูลการรวมแบบสองทิศทางในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3cc2a-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3cc2a-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3cc2a-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3cc2a-105">กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาด้วยโมดูล **การรวมแบบสองทิศทาง** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3cc2a-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cc2a-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="3cc2a-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3cc2a-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3cc2a-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="3cc2a-108">คุณไม่สามารถโหลดโมดูลการรวมแบบสองทิศทางในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3cc2a-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="3cc2a-109">หากคุณไม่สามารถเปิดหน้า **การรวมแบบสองทิศทาง** โดยการเลือกไทล์ **การรวมแบบสองทิศทาง** ในพื้นที่ทำงาน **การจัดการข้อมูล** บริการการรวมข้อมูลอาจหยุดทำงานได้</span><span class="sxs-lookup"><span data-stu-id="3cc2a-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="3cc2a-110">สร้างบัตรผ่านการสนับสนุนเพื่อร้องขอการรีสตาร์ทของบริการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3cc2a-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="3cc2a-111">ข้อผิดพลาดเมื่อคุณพยายามสร้างการแม็ปเอนทิตี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="3cc2a-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="3cc2a-112">**ข้อมูลประจำตัวที่จำเป็นในแก้ปัญหา:** ผู้ดูแลระบบผู้เช่า Azure AD</span><span class="sxs-lookup"><span data-stu-id="3cc2a-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="3cc2a-113">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามตั้งค่าคอนฟิกเอนทิตี้ใหม่สำหรับการรวมแบบสองทิศทาง:</span><span class="sxs-lookup"><span data-stu-id="3cc2a-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="3cc2a-114">*รหัสสถานะการตอบสนองไม่บ่งชี้ความสำเร็จ: 401 (ไม่ได้รับอนุมัติ)*</span><span class="sxs-lookup"><span data-stu-id="3cc2a-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="3cc2a-115">ข้อผิดพลาดนี้เกิดขึ้นเนื่องจากเฉพาะผู้ดูแลระบบผู้เช่า Azure AD เท่านั้นที่สามารถเพิ่มการแม็ปเอนทิตี้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="3cc2a-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="3cc2a-116">เมื่อต้องการแก้ไขปัญหานี้ ให้ลงชื่อเข้าใช้ในแอป Finance and Operations ในฐานะผู้เช่าของผู้ดูแลระบบ Azure AD</span><span class="sxs-lookup"><span data-stu-id="3cc2a-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="3cc2a-117">นอกจากนี้ คุณต้องไปที่ web.PowerApps.com และตรวจสอบความถูกต้องการเชื่อมต่อของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3cc2a-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="3cc2a-118">ข้อผิดพลาดเมื่อคุณเปิดอินเทอร์เฟสผู้ใช้การรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="3cc2a-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="3cc2a-119">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามเข้าถึงการรวมแบบสองทิศทางจากพื้นที่ทำงาน **การจัดการข้อมูล**:</span><span class="sxs-lookup"><span data-stu-id="3cc2a-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="3cc2a-120">*login.microsoftonline.com ปฏิเสธที่จะเชื่อมต่อ*</span><span class="sxs-lookup"><span data-stu-id="3cc2a-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="3cc2a-121">เมื่อต้องการแก้ไขปัญหานี้ ให้ลงชื่อเข้าใช้โดยใช้หน้าต่างแบบ InPrivate ใน Microsoft Edge หน้าต่างที่ไม่ระบุตัวตนใน Chromium หรือหน้าต่างที่ไม่ระบุตัวตนใน Google Chrome</span><span class="sxs-lookup"><span data-stu-id="3cc2a-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="3cc2a-122">นอกจากนี้ คุณยังต้องยกเลิกการบล็อคหรือล้างคุกกี้ของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="3cc2a-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="3cc2a-123">ข้อผิดพลาดเมื่อคุณเชื่อมโยงสภาพแวดล้อมสำหรับการรวมแบบสองทิศทาง หรือเพิ่มการแม็ปเอนทิตี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="3cc2a-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="3cc2a-124">**ข้อมูลประจำตัวที่จำเป็นในแก้ปัญหา:** ผู้ดูแลระบบผู้เช่า Azure AD</span><span class="sxs-lookup"><span data-stu-id="3cc2a-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="3cc2a-125">คุณอาจพบข้อผิดพลาดต่อไปนี้ เมื่อเชื่อมโยงหรือสร้างแผนที่:</span><span class="sxs-lookup"><span data-stu-id="3cc2a-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="3cc2a-126">*รหัสสถานะการตอบสนองไม่บ่งชี้ความสำเร็จ: 403 (tokenexchange)<br> รหัสรอบเวลา: \<รหัสรอบเวลาของคุณ\><br> รหัสกิจกรรมของราก: \<รหัสกิจกรรมรากของคุณ\>*</span><span class="sxs-lookup"><span data-stu-id="3cc2a-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="3cc2a-127">ข้อผิดพลาดนี้อาจเกิดขึ้นได้ ถ้าคุณไม่มีสิทธิ์เพียงพอที่จะเชื่อมโยงการรวมแบบสองทิศทาง หรือสร้างแผนที่</span><span class="sxs-lookup"><span data-stu-id="3cc2a-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="3cc2a-128">คุณต้องใช้บัญชีผู้ดูแลระบบผู้เช่า Azure AD เพื่อเชื่อมโยงสภาพแวดล้อม และเพิ่มการแม็ปเอนทิตี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="3cc2a-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="3cc2a-129">อย่างไรก็ตาม หลังจากการตั้งค่า คุณสามารถใช้บัญชีที่ไม่ใช่ผู้ดูแลระบบเพื่อตรวจสอบสถานะและแก้ไขการแม็ป</span><span class="sxs-lookup"><span data-stu-id="3cc2a-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="3cc2a-130">ข้อผิดพลาดเมื่อคุณหยุดการแม็ปเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3cc2a-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="3cc2a-131">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามที่จะหยุดการแม็ปเอนทิตี้:</span><span class="sxs-lookup"><span data-stu-id="3cc2a-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="3cc2a-132">*\[ไม่ได้รับอนุญาต\] \[{"สถานะ":403,"แหล่งข้อมูล":"","ข้อความ":"ข้อผิดพลาดจากการแลกเปลี่ยนโทเคน: ผู้ใช้ไม่ได้รับอนุญาตให้เข้าถึงการเชื่อมต่อ dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต*</span><span class="sxs-lookup"><span data-stu-id="3cc2a-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="3cc2a-133">ข้อผิดพลาดนี้จะเกิดขึ้น เมื่อสภาพแวดล้อม Common Data Service ที่มีการเชื่อมโยงไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3cc2a-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="3cc2a-134">เมื่อต้องการแก้ไขปัญหา ให้สร้างตั๋วสำหรับทีมงานการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3cc2a-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="3cc2a-135">แนบการสืบค้นกลับเครือข่ายเพื่อให้ทีมงานการรวมข้อมูลสามารถทำเครื่องหมายแผนที่เป็น **ไม่ได้รันอยู่** ในแบ็คเอนด์</span><span class="sxs-lookup"><span data-stu-id="3cc2a-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
