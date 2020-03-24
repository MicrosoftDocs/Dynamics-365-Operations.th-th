---
title: คุณลักษณะแพลตฟอร์มที่ถูกลบออกหรือเลิกสนับสนุน
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจากการอัปเดตแพลตฟอร์มของแอป Finance and Operations
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095785"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="70ec3-103">คุณลักษณะแพลตฟอร์มที่ถูกลบออกหรือเลิกสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="70ec3-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70ec3-104">หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจากการอัปเดตแพลตฟอร์มของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70ec3-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="70ec3-105">คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="70ec3-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="70ec3-106">คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="70ec3-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="70ec3-107">รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="70ec3-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="70ec3-108">ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)</span><span class="sxs-lookup"><span data-stu-id="70ec3-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="70ec3-109">คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70ec3-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="70ec3-110">แพลตฟอร์ม update 32</span><span class="sxs-lookup"><span data-stu-id="70ec3-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="70ec3-111">กล่องโต้ตอบการเปลี่ยนแปลงคำขอของลำดับงานไม่รวมรายการแบบหล่นลงของการเลือกผู้ใช้ไว้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="70ec3-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="70ec3-112">**เหตุผลสำหรับการยกเลิกการใช้/การลบ**</span><span class="sxs-lookup"><span data-stu-id="70ec3-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="70ec3-113">นี่เป็นปัญหาด้านความปลอดภัยเนื่องจากไม่สามารถส่งคำขอเปลี่ยนแปลงไปยังผู้ใช้ที่ไม่ได้จัดทำขึ้น</span><span class="sxs-lookup"><span data-stu-id="70ec3-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="70ec3-114">นี่ยังเป็นปัญหาของการใช้ เนื่องจากมีการนำผู้ใช้นี้ไปใช้ในการกำหนดผู้ริเริ่มลำดับงานและเลือกด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="70ec3-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="70ec3-115">**แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="70ec3-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="70ec3-116">ไม่</span><span class="sxs-lookup"><span data-stu-id="70ec3-116">No</span></span> |
| <span data-ttu-id="70ec3-117">**พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**</span><span class="sxs-lookup"><span data-stu-id="70ec3-117">**Product areas affected**</span></span>         | <span data-ttu-id="70ec3-118">ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="70ec3-118">Workflow</span></span> |
| <span data-ttu-id="70ec3-119">**ตัวเลือกการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="70ec3-119">**Deployment option**</span></span>              | <span data-ttu-id="70ec3-120">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="70ec3-120">All</span></span> |
| <span data-ttu-id="70ec3-121">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="70ec3-121">**Status**</span></span>                         | <span data-ttu-id="70ec3-122">รายการแบบหล่นลงของการเลือกผู้ใช้ถูกลบออกจากกล่องโต้ตอบการเปลี่ยนแปลงคำขอในการอัปเดตแพลตฟอร์มที่ 32</span><span class="sxs-lookup"><span data-stu-id="70ec3-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="70ec3-123">การร้องขอการเปลี่ยนแปลงคำขอจะถูกส่งไปยังผู้ริเริ่มโดยอัตโนมัติตามที่จัดทำขึ้นไว้</span><span class="sxs-lookup"><span data-stu-id="70ec3-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="70ec3-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันนี้ ให้ดูที่ [การดำเนินการในกระบวนการอนุมัติลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)</span><span class="sxs-lookup"><span data-stu-id="70ec3-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a><span data-ttu-id="70ec3-125">ไม่สนับสนุนการเชื่อมโยงแบบลงรายละเอียดแบบฝังในเอกสารที่ใส่เลขหน้าของเอกสารซึ่งแสดงโดยบริการที่โฮสต์แบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="70ec3-125">Embedded drill-through links are no longer supported in paginated documents rendered by the cloud-hosted service</span></span> 
|   |  |
|------------|--------------------|
| <span data-ttu-id="70ec3-126">**เหตุผลสำหรับการยกเลิกการใช้/การลบ**</span><span class="sxs-lookup"><span data-stu-id="70ec3-126">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="70ec3-127">URL การนำทางที่ฝังอยู่ในเอกสารที่แสดงโดยบริการ อาจประกอบด้วยข้อมูลทางธุรกิจที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="70ec3-127">Navigation URLs embedded in documents rendered by the service may contain sensitive business data.</span></span> <span data-ttu-id="70ec3-128">เรากำลังลบการสนับสนุนสำหรับการเชื่อมโยงแบบลงรายละเอียดแบบฝังในเอกสารเป็นข้อควรระวังด้านการรักษาความปลอดภัย เพื่อปกป้องข้อมูลของลูกค้าเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="70ec3-128">We are removing support for embedded drill-through links in documents as a security precaution to further protect customer's data.</span></span> <span data-ttu-id="70ec3-129">นอกจากนี้ ผู้ใช้ยังได้รับประโยชน์จากประสิทธิภาพที่ดียิ่งขึ้น ในขณะที่มีการผลิตเอกสารที่มีการโต้ตอบซึ่งเป็นผลมาจากการเปลี่ยนแปลงนี้</span><span class="sxs-lookup"><span data-stu-id="70ec3-129">Users will also benefit from improved performance while interactively producing documents as a result of this change.</span></span>  |
| <span data-ttu-id="70ec3-130">**แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="70ec3-130">**Replaced by another feature?**</span></span>   | <span data-ttu-id="70ec3-131">จำนวน</span><span class="sxs-lookup"><span data-stu-id="70ec3-131">No</span></span> |
| <span data-ttu-id="70ec3-132">**พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**</span><span class="sxs-lookup"><span data-stu-id="70ec3-132">**Product areas affected**</span></span>         | <span data-ttu-id="70ec3-133">การรายงาน</span><span class="sxs-lookup"><span data-stu-id="70ec3-133">Reporting</span></span> |
| <span data-ttu-id="70ec3-134">**ตัวเลือกการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="70ec3-134">**Deployment option**</span></span>              | <span data-ttu-id="70ec3-135">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="70ec3-135">All</span></span> |
| <span data-ttu-id="70ec3-136">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="70ec3-136">**Status**</span></span>                         | <span data-ttu-id="70ec3-137">คุณลักษณะนี้ถูกลบออกจากบริการ</span><span class="sxs-lookup"><span data-stu-id="70ec3-137">This feature is actively being removed from the service.</span></span><br><br><span data-ttu-id="70ec3-138">ไคลเอนต์ที่ทันสมัยมีตัวเลือกมากมายสำหรับการผลิตมุมมองที่มีการเชื่อมโยงที่สร้างขึ้นโดยอัตโนมัติ เพื่อให้ความช่วยเหลือในการนำทางของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="70ec3-138">The modern client offers numerous options for producing views that include auto-generated links to assist in navigating the application.</span></span> <span data-ttu-id="70ec3-139">ขอแนะนำให้ใช้เอกสารที่ใส่เลขหน้าของเอกสารซึ่งแสดงโดยบริการสำหรับการสื่อสารภายนอกที่มีการส่งอีเมล เก็บถาวร และพิมพ์ สำหรับผู้รับ</span><span class="sxs-lookup"><span data-stu-id="70ec3-139">Paginated documents rendered by the service are recommended for external communications that are emailed, archived, and printed for recipients.</span></span> <span data-ttu-id="70ec3-140">เราได้ปรับปรุงประสบการณ์ในการแสดงตัวอย่างเอกสารโดยตรงในเบราว์เซอร์ ซึ่งมีสิทธิ์เข้าถึงเครื่องพิมพ์เฉพาะที่โดยตรง</span><span class="sxs-lookup"><span data-stu-id="70ec3-140">We have improved the experience for previewing documents directly in the browser, which offers direct access to local printers.</span></span> <span data-ttu-id="70ec3-141">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [แสดงตัวอย่างเอกสาร PDF ที่มีตัวแสดงที่ฝังอยู่](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents)</span><span class="sxs-lookup"><span data-stu-id="70ec3-141">For more information, see [Preview PDF documents with an embedded viewer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="70ec3-142">ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="70ec3-142">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="70ec3-143">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../migration-upgrade/deprecated-features.md)</span><span class="sxs-lookup"><span data-stu-id="70ec3-143">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

