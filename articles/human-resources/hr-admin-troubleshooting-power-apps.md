---
title: ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps
description: บทความนี้อธิบายสิ่งที่ต้องทำ หากผู้ดูแลไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420741"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="a7e5c-103">ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps</span><span class="sxs-lookup"><span data-stu-id="a7e5c-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="a7e5c-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a7e5c-104">**Issue**</span></span>

- <span data-ttu-id="a7e5c-105">ผู้เช่า/ผู้ดูแลสภาพแวดล้อมไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="a7e5c-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="a7e5c-106">ยังไม่มีการกำหนดลิขสิทธิ์ที่ให้ผู้ใช้มีสิทธิ์ในการดำเนินการขั้นตอนการสร้างสภาพแวดล้อมให้ผู้ใช้ที่กำลังดำเนินการขั้นตอนนั้นโดยตรง</span><span class="sxs-lookup"><span data-stu-id="a7e5c-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="a7e5c-107">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="a7e5c-107">**Solution**</span></span>

<span data-ttu-id="a7e5c-108">ตรวจสอบให้แน่ใจว่า ผู้ดูแลระบบผู้เช่าได้กำหนดให้ลิขสิทธิ์ Power Apps P2 ที่ถูกต้องโดยตรงให้กับผู้ใช้ที่จะดำเนินการขั้นตอนการสร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="a7e5c-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="a7e5c-109">นี่คือแผนบริการ Microsoft Dynamics ที่ให้สิทธิ์นั้น</span><span class="sxs-lookup"><span data-stu-id="a7e5c-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="a7e5c-110">หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)</span><span class="sxs-lookup"><span data-stu-id="a7e5c-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="a7e5c-111">Power Apps แผนบริการ P2</span><span class="sxs-lookup"><span data-stu-id="a7e5c-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="a7e5c-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="a7e5c-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="a7e5c-113">Power Apps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a7e5c-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="a7e5c-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="a7e5c-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="a7e5c-115">Power Apps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a7e5c-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="a7e5c-116">โปรดทราบว่า Microsoft Office SKU ที่หลากหลายยังให้สิทธิ์ พร้อมกับ Power Apps Plan 2 SKUs แบบสแตนด์อโลนอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="a7e5c-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="a7e5c-117">จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่</span><span class="sxs-lookup"><span data-stu-id="a7e5c-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="a7e5c-118">ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)</span><span class="sxs-lookup"><span data-stu-id="a7e5c-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="a7e5c-119">สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [การเตรียมใช้งานทรัพยากรบุคคล](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="a7e5c-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
