---
title: คุณลักษณะแพลตฟอร์มที่ถูกลบออกหรือเลิกสนับสนุน
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจากการอัปเดตแพลตฟอร์มของแอป Finance and Operations
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
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
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087894"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="d3dd1-103">คุณลักษณะแพลตฟอร์มที่ถูกลบออกหรือเลิกสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d3dd1-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3dd1-104">หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจากการอัปเดตแพลตฟอร์มของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3dd1-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="d3dd1-105">คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d3dd1-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="d3dd1-106">คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="d3dd1-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="d3dd1-107">รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="d3dd1-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="d3dd1-108">ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)</span><span class="sxs-lookup"><span data-stu-id="d3dd1-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="d3dd1-109">คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3dd1-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="d3dd1-110">แพลตฟอร์ม update 32</span><span class="sxs-lookup"><span data-stu-id="d3dd1-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="d3dd1-111">กล่องโต้ตอบการเปลี่ยนแปลงคำขอของลำดับงานไม่รวมรายการแบบหล่นลงของการเลือกผู้ใช้ไว้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d3dd1-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="d3dd1-112">**เหตุผลสำหรับการยกเลิกการใช้/การลบ**</span><span class="sxs-lookup"><span data-stu-id="d3dd1-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d3dd1-113">นี่เป็นปัญหาด้านความปลอดภัยเนื่องจากไม่สามารถส่งคำขอเปลี่ยนแปลงไปยังผู้ใช้ที่ไม่ได้จัดทำขึ้น</span><span class="sxs-lookup"><span data-stu-id="d3dd1-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="d3dd1-114">นี่ยังเป็นปัญหาของการใช้ เนื่องจากมีการนำผู้ใช้นี้ไปใช้ในการกำหนดผู้ริเริ่มลำดับงานและเลือกด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d3dd1-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="d3dd1-115">**แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="d3dd1-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d3dd1-116">ไม่</span><span class="sxs-lookup"><span data-stu-id="d3dd1-116">No</span></span> |
| <span data-ttu-id="d3dd1-117">**พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**</span><span class="sxs-lookup"><span data-stu-id="d3dd1-117">**Product areas affected**</span></span>         | <span data-ttu-id="d3dd1-118">ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="d3dd1-118">Workflow</span></span> |
| <span data-ttu-id="d3dd1-119">**ตัวเลือกการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="d3dd1-119">**Deployment option**</span></span>              | <span data-ttu-id="d3dd1-120">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d3dd1-120">All</span></span> |
| <span data-ttu-id="d3dd1-121">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="d3dd1-121">**Status**</span></span>                         | <span data-ttu-id="d3dd1-122">รายการแบบหล่นลงของการเลือกผู้ใช้ถูกลบออกจากกล่องโต้ตอบการเปลี่ยนแปลงคำขอในการอัปเดตแพลตฟอร์มที่ 32</span><span class="sxs-lookup"><span data-stu-id="d3dd1-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="d3dd1-123">การร้องขอการเปลี่ยนแปลงคำขอจะถูกส่งไปยังผู้ริเริ่มโดยอัตโนมัติตามที่จัดทำขึ้นไว้</span><span class="sxs-lookup"><span data-stu-id="d3dd1-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="d3dd1-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันนี้ ให้ดูที่ [การดำเนินการในกระบวนการอนุมัติลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)</span><span class="sxs-lookup"><span data-stu-id="d3dd1-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="d3dd1-125">ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d3dd1-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="d3dd1-126">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../migration-upgrade/deprecated-features.md)</span><span class="sxs-lookup"><span data-stu-id="d3dd1-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

