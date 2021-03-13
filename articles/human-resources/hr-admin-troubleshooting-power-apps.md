---
title: ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps
description: บทความนี้อธิบายสิ่งที่ต้องทำ หากผู้ดูแลไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114445"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="3ba4a-103">ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps</span><span class="sxs-lookup"><span data-stu-id="3ba4a-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="3ba4a-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="3ba4a-104">**Issue**</span></span>

- <span data-ttu-id="3ba4a-105">ผู้เช่า/ผู้ดูแลสภาพแวดล้อมไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="3ba4a-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="3ba4a-106">ผู้ใช้ไม่มีลิขสิทธิ์ที่มีสิทธิสร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="3ba4a-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="3ba4a-107">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="3ba4a-107">**Solution**</span></span>

<span data-ttu-id="3ba4a-108">ตรวจสอบให้แน่ใจว่าผู้ดูแลระบบผู้เช่าได้มอบหมายลิขสิทธิ์ Power Apps P2 ที่ถูกต้องให้กับผู้ใช้ที่สร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="3ba4a-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="3ba4a-109">แผนบริการ Microsoft Dynamics ต่อไปนี้จะให้สิทธิ์ในการสร้างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="3ba4a-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="3ba4a-110">หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)</span><span class="sxs-lookup"><span data-stu-id="3ba4a-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="3ba4a-111">Power Apps แผนบริการ P2</span><span class="sxs-lookup"><span data-stu-id="3ba4a-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="3ba4a-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="3ba4a-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="3ba4a-113">Power Apps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3ba4a-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="3ba4a-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3ba4a-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="3ba4a-115">Power Apps สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3ba4a-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="3ba4a-116">โปรดทราบว่า Microsoft Office SKU ที่หลากหลายยังให้สิทธิ์ พร้อมกับ Power Apps Plan 2 SKUs แบบสแตนด์อโลนอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="3ba4a-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="3ba4a-117">จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่</span><span class="sxs-lookup"><span data-stu-id="3ba4a-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="3ba4a-118">ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)</span><span class="sxs-lookup"><span data-stu-id="3ba4a-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="3ba4a-119">สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [การเตรียมใช้งานทรัพยากรบุคคล](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="3ba4a-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
