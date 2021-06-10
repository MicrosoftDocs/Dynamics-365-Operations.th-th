---
title: ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps
description: บทความนี้อธิบายสิ่งที่ต้องทำ หากผู้ดูแลไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053358"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="f4cc0-103">ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps</span><span class="sxs-lookup"><span data-stu-id="f4cc0-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f4cc0-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="f4cc0-104">**Issue**</span></span>

- <span data-ttu-id="f4cc0-105">ผู้เช่า/ผู้ดูแลสภาพแวดล้อมไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="f4cc0-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="f4cc0-106">ผู้ใช้ไม่มีลิขสิทธิ์ที่มีสิทธิสร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f4cc0-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="f4cc0-107">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="f4cc0-107">**Solution**</span></span>

<span data-ttu-id="f4cc0-108">ตรวจสอบให้แน่ใจว่าผู้ดูแลระบบผู้เช่าได้มอบหมายลิขสิทธิ์ Power Apps P2 ที่ถูกต้องให้กับผู้ใช้ที่สร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f4cc0-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="f4cc0-109">แผนบริการ Microsoft Dynamics ต่อไปนี้จะให้สิทธิ์ในการสร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f4cc0-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="f4cc0-110">หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)</span><span class="sxs-lookup"><span data-stu-id="f4cc0-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="f4cc0-111">Power Apps แผนบริการ P2</span><span class="sxs-lookup"><span data-stu-id="f4cc0-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="f4cc0-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="f4cc0-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="f4cc0-113">Power Apps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f4cc0-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="f4cc0-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="f4cc0-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="f4cc0-115">Power Apps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f4cc0-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="f4cc0-116">โปรดทราบว่า Microsoft Office SKU ที่หลากหลายยังให้สิทธิ์ พร้อมกับ Power Apps Plan 2 SKUs แบบสแตนด์อโลนอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="f4cc0-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="f4cc0-117">จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่</span><span class="sxs-lookup"><span data-stu-id="f4cc0-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="f4cc0-118">ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)</span><span class="sxs-lookup"><span data-stu-id="f4cc0-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="f4cc0-119">สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [การเตรียมใช้งานทรัพยากรบุคคล](/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="f4cc0-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]