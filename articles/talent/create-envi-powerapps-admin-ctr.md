---
title: ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ PowerApps ได้
description: หัวข้อนี้อธิบายสิ่งที่ต้องทำ หากผู้ดูแลไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft PowerApps
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519173"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="264f3-103">ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ PowerApps</span><span class="sxs-lookup"><span data-stu-id="264f3-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="264f3-104">**ออก**</span><span class="sxs-lookup"><span data-stu-id="264f3-104">**Issue**</span></span>

- <span data-ttu-id="264f3-105">ผู้เช่า/ผู้ดูแลสภาพแวดล้อมไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="264f3-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="264f3-106">ยังไม่มีการกำหนดลิขสิทธิ์ที่ให้ผู้ใช้มีสิทธิ์ในการดำเนินการขั้นตอนการสร้างสภาพแวดล้อมให้ผู้ใช้ที่กำลังดำเนินการขั้นตอนนั้นโดยตรง</span><span class="sxs-lookup"><span data-stu-id="264f3-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="264f3-107">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="264f3-107">**Solution**</span></span>

<span data-ttu-id="264f3-108">ตรวจสอบให้แน่ใจว่า ผู้ดูแลระบบผู้เช่าได้กำหนดให้ลิขสิทธิ์ PowerApps P2 ที่ถูกต้องโดยตรงให้กับผู้ใช้ที่จะดำเนินการขั้นตอนการสร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="264f3-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="264f3-109">นี่คือแผนบริการ Microsoft Dynamics ที่ให้สิทธิ์นั้น</span><span class="sxs-lookup"><span data-stu-id="264f3-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="264f3-110">หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)</span><span class="sxs-lookup"><span data-stu-id="264f3-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="264f3-111">แผนการบริการ PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="264f3-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="264f3-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="264f3-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="264f3-113">PowerApps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="264f3-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="264f3-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="264f3-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="264f3-115">PowerApps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="264f3-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="264f3-116">โปรดทราบว่า Microsoft Office SKU ที่หลากหลายยังให้สิทธิ์ พร้อมกับ PowerApps Plan 2 SKUs แบบสแตนด์อโลนอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="264f3-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="264f3-117">จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่</span><span class="sxs-lookup"><span data-stu-id="264f3-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="264f3-118">ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)</span><span class="sxs-lookup"><span data-stu-id="264f3-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="264f3-119">สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="264f3-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
