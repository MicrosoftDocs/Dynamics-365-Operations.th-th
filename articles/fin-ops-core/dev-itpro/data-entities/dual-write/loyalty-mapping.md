---
title: บัตรสมาชิกของลูกค้าและคะแนนรางวัล
description: หัวข้อนี้จะอธิบายถึงการรวมข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้าและคะแนนรางวัลระหว่างแอป Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
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
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172980"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="e0ca8-103">บัตรสมาชิกของลูกค้าและคะแนนรางวัล</span><span class="sxs-lookup"><span data-stu-id="e0ca8-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e0ca8-104">ธุรกิจจะจัดประเภทลูกค้าและให้บริการที่ซับซ้อนตามการซื้อของลูกค้าและรูปแบบการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e0ca8-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="e0ca8-105">ในชุดแอพลิเคชัน Microsoft Dynamics 365 Dynamics 365 Commerce มีโครงสร้างพื้นฐานและฟังก์ชันเพื่ออำนวยความสะดวกและจัดการบัตรสมาชิกของลูกค้า คะแนนรางวัล การกำหนดราคาตามความภักดี และประสบการณ์การซื้อตามรางวัล</span><span class="sxs-lookup"><span data-stu-id="e0ca8-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="e0ca8-106">เมื่อข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้าและคะแนนรางวัลใน Commerce ถูกซิงค์ไปยัง Common Data service แอปที่เป็นแบบโมเดลใน Dynamics 365 สามารถใช้ข้อมูลนั้นได้</span><span class="sxs-lookup"><span data-stu-id="e0ca8-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="e0ca8-107">ตัวอย่างเช่น ผู้ใช้ Dynamics 365 Customer Service สามารถใช้ข้อมูลเพื่อให้บริการแบบซับซ้อนเดียวกันผ่านทางฝ่ายช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="e0ca8-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="e0ca8-108">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="e0ca8-108">Templates</span></span>

| <span data-ttu-id="e0ca8-109">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e0ca8-109">Finance and Operations apps</span></span> | <span data-ttu-id="e0ca8-110">แอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e0ca8-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e0ca8-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e0ca8-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="e0ca8-112">บัตรสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e0ca8-112">Loyalty card</span></span>                | <span data-ttu-id="e0ca8-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="e0ca8-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="e0ca8-114">เท็มเพลตนี้จะซิงค์ข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e0ca8-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="e0ca8-115">คะแนนรางวัลสำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e0ca8-115">Loyalty reward points</span></span>       | <span data-ttu-id="e0ca8-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="e0ca8-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="e0ca8-117">เท็มเพลตนี้จะซิงค์ข้อมูลเกี่ยวกับคะแนนรางวัลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e0ca8-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
