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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683634"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="2d970-103">แก้ไขปัญหาเกี่ยวกับโมดูลการรวมแบบสองทิศทางในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d970-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2d970-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="2d970-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="2d970-105">กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาด้วยโมดูล **การรวมแบบสองทิศทาง** ในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d970-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d970-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="2d970-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="2d970-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2d970-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="2d970-108">คุณไม่สามารถโหลดโมดูลการรวมแบบสองทิศทางในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d970-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="2d970-109">หากคุณไม่สามารถเปิดหน้า **การรวมแบบสองทิศทาง** โดยการเลือกไทล์ **การรวมแบบสองทิศทาง** ในพื้นที่ทำงาน **การจัดการข้อมูล** บริการการรวมข้อมูลอาจหยุดทำงานได้</span><span class="sxs-lookup"><span data-stu-id="2d970-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="2d970-110">สร้างบัตรผ่านการสนับสนุนเพื่อร้องขอการรีสตาร์ทของบริการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2d970-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="2d970-111">ข้อผิดพลาดเมื่อคุณพยายามสร้างแผนที่ตารางใหม่</span><span class="sxs-lookup"><span data-stu-id="2d970-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="2d970-112">**ข้อมูลประจำตัวที่จำเป็นในการแก้ไขปัญหา:** ผู้ใช้เดียวกันที่ตั้งค่าการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="2d970-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="2d970-113">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามตั้งค่าคอนฟิกเอนทิตี้ใหม่สำหรับการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="2d970-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="2d970-114">ผู้ใช้เท่านั้นที่สามารถสร้างแผนที่ได้คือ ผู้ใช้ที่ตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="2d970-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="2d970-115">*รหัสสถานะการตอบสนองไม่บ่งชี้ความสำเร็จ: 401 (ไม่ได้รับอนุมัติ)*</span><span class="sxs-lookup"><span data-stu-id="2d970-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="2d970-116">ข้อผิดพลาดเมื่อคุณเปิดอินเทอร์เฟสผู้ใช้การรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="2d970-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="2d970-117">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามเข้าถึงการรวมแบบสองทิศทางจากพื้นที่ทำงาน **การจัดการข้อมูล**:</span><span class="sxs-lookup"><span data-stu-id="2d970-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="2d970-118">*login.microsoftonline.com ปฏิเสธที่จะเชื่อมต่อ*</span><span class="sxs-lookup"><span data-stu-id="2d970-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="2d970-119">เมื่อต้องการแก้ไขปัญหานี้ ให้ลงชื่อเข้าใช้โดยใช้หน้าต่างแบบ InPrivate ใน Microsoft Edge หน้าต่างที่ไม่ระบุตัวตนใน Chromium หรือหน้าต่างที่ไม่ระบุตัวตนใน Google Chrome</span><span class="sxs-lookup"><span data-stu-id="2d970-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="2d970-120">นอกจากนี้ คุณยังต้องยกเลิกการบล็อคหรือล้างคุกกี้ของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="2d970-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="2d970-121">ข้อผิดพลาดเมื่อคุณเชื่อมโยงสภาพแวดล้อมสำหรับการรวมแบบสองทิศทาง หรือเพิ่มการแม็ปตารางใหม่</span><span class="sxs-lookup"><span data-stu-id="2d970-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="2d970-122">**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบในทั้งแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="2d970-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="2d970-123">คุณอาจพบข้อผิดพลาดต่อไปนี้ เมื่อเชื่อมโยงหรือสร้างแผนที่:</span><span class="sxs-lookup"><span data-stu-id="2d970-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="2d970-124">*รหัสสถานะการตอบสนองไม่บ่งชี้ความสำเร็จ: 403 (tokenexchange)<br> รหัสรอบเวลา: \<your session id\><br> รหัสกิจกรรมของราก: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="2d970-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="2d970-125">ข้อผิดพลาดนี้อาจเกิดขึ้นได้ ถ้าคุณไม่มีสิทธิ์เพียงพอที่จะเชื่อมโยงการรวมแบบสองทิศทาง หรือสร้างแผนที่</span><span class="sxs-lookup"><span data-stu-id="2d970-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="2d970-126">นอกจากนี้ ข้อผิดพลาดนี้ยังอาจเกิดขึ้น ถ้าสภาพแวดล้อม Dataverse ถูกรีเซ็ตโดยไม่มีการยกเลิกการเชื่อมโยงการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="2d970-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="2d970-127">ผู้ใช้ที่มีบทบาทผู้ดูแลระบบในทั้งแอป Finance and Operations และ Dataverse สามารถเชื่อมโยงสภาพแวดล้อมได้</span><span class="sxs-lookup"><span data-stu-id="2d970-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="2d970-128">เฉพาะผู้ใช้ที่ตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางเท่านั้นที่สามารถเพิ่มแผนที่ตารางใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="2d970-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="2d970-129">หลังจากการตั้งค่า ผู้ใช้ใดๆ ที่มีบทบาทผู้ดูแลระบบสามารถตรวจสอบสถานะและแก้ไขการแม็ปได้</span><span class="sxs-lookup"><span data-stu-id="2d970-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="2d970-130">ข้อผิดพลาดเมื่อคุณหยุดการแม็ปตาราง</span><span class="sxs-lookup"><span data-stu-id="2d970-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="2d970-131">คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามที่จะหยุดการแม็ปตาราง:</span><span class="sxs-lookup"><span data-stu-id="2d970-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="2d970-132">*\[ไม่ได้รับอนุญาต\] \[{"สถานะ":403,"แหล่งข้อมูล":"","ข้อความ":"ข้อผิดพลาดจากการแลกเปลี่ยนโทเคน: ผู้ใช้ไม่ได้รับอนุญาตให้เข้าถึงการเชื่อมต่อ dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต*</span><span class="sxs-lookup"><span data-stu-id="2d970-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="2d970-133">ข้อผิดพลาดนี้จะเกิดขึ้น เมื่อสภาพแวดล้อม Dataverse ที่มีการเชื่อมโยงไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2d970-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="2d970-134">เมื่อต้องการแก้ไขปัญหา ให้สร้างตั๋วสำหรับทีมงานการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2d970-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="2d970-135">แนบการสืบค้นกลับเครือข่ายเพื่อให้ทีมงานการรวมข้อมูลสามารถทำเครื่องหมายแผนที่เป็น **ไม่ได้รันอยู่** ในแบ็คเอนด์</span><span class="sxs-lookup"><span data-stu-id="2d970-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-table-mapping"></a><span data-ttu-id="2d970-136">เกิดข้อผิดพลาดในขณะที่พยายามเริ่มต้นการแม็ปตาราง</span><span class="sxs-lookup"><span data-stu-id="2d970-136">Error while trying to start an table mapping</span></span>

<span data-ttu-id="2d970-137">คุณอาจได้รับข้อผิดพลาดดังเช่นต่อไปนี้ เมื่อคุณพยายามตั้งค่าสถานะดังกล่าวของการแม็ปเป็น **กำลังรัน**:</span><span class="sxs-lookup"><span data-stu-id="2d970-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="2d970-138">*ไม่สามารถทำการซิงค์ข้อมูลเริ่มต้นให้เสร็จสมบูรณ์ได้ ข้อผิดพลาด: ความล้มเหลวในการรวมแบบสองทิศทาง - การลงทะเบียนปลั๊กอินล้มเหลว: ไม่สามารถสร้างข้อมูลเมตาในการค้นหาการรวมแบบสองทิศทางได้ ไม่ได้ตั้งค่าการอ้างอิงอ็อบเจกต์ข้อผิดพลาดให้กับอินสแตนซ์ของอ็อบเจ็กต์*</span><span class="sxs-lookup"><span data-stu-id="2d970-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="2d970-139">การแก้ไขสำหรับข้อผิดพลาดนี้จะขึ้นอยู่กับสาเหตุของข้อผิดพลาด:</span><span class="sxs-lookup"><span data-stu-id="2d970-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="2d970-140">ถ้าการแม็ปมีการแม็ปที่ไม่ขึ้นต่อกัน ให้ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการแม็ปที่ไม่ขึ้นต่อกันของการแม็ปตารางนี้</span><span class="sxs-lookup"><span data-stu-id="2d970-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="2d970-141">การแม็ปอาจขาดฟิลด์ต้นทางหรือปลายทาง</span><span class="sxs-lookup"><span data-stu-id="2d970-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="2d970-142">ถ้าฟิลด์ในแอป Finance and Operations ขาดหายไป ให้ทำตามขั้นตอนในส่วน [ปัญหาฟิลด์เอนทิตี้ที่หายไปบนแผนที่](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps)</span><span class="sxs-lookup"><span data-stu-id="2d970-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="2d970-143">ถ้าฟิลด์ใน Dataverse ขาดหายไป ให้คลิกปุ่ม **รีเฟรชตาราง** บนการแม็ป เพื่อให้มีการเติมข้อมูลในฟิลด์โดยอัตโนมัติกลับไปยังการแม็ป</span><span class="sxs-lookup"><span data-stu-id="2d970-143">If a field in Dataverse is missing, then click **Refresh tables** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
