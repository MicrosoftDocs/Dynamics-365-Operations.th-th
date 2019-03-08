---
title: การกระจายในรายงานค่าใช้จ่าย
description: เมื่อคุณป้อนค่าใช้จ่ายในรายงานค่าใช้จ่าย คุณสามารถกระจายค่าใช้จ่ายระหว่างโครงการ นิติบุคคล หรือบัญชีหลายรายการในองค์กรของคุณ
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00d051a8f644a6a0bedb0acc3eaac9a3dd1109e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "356771"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="44213-103">การกระจายในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="44213-103">Distributions on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44213-104"> เมื่อคุณป้อนค่าใช้จ่ายในรายงานค่าใช้จ่าย คุณสามารถกระจายค่าใช้จ่ายระหว่างโครงการ มิติทางการเงิน หรือบัญชีหลายรายการในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="44213-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="44213-105">ตัวอย่างเช่น Nancy พนักงานขาย Fabrikam เดินทางจากโคเปนเฮเกนไปแฟรงค์เฟิร์ต</span><span class="sxs-lookup"><span data-stu-id="44213-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="44213-106">ในแฟรงค์เฟิร์ต เธอพบกับองค์กรสองแห่งเพื่อพูดคุยเกี่ยวกับโครงการที่ต่างกันสำหรับแต่ละองค์กร</span><span class="sxs-lookup"><span data-stu-id="44213-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="44213-107">Nancy ใช้เวลาเจ็ดวันทำการในการทำงานกับองค์กร A เกี่ยวกับโครงการ A และใช้เวลาสามวันทำการในการทำงานกับองค์กร B เกี่ยวกับโครงการ B</span><span class="sxs-lookup"><span data-stu-id="44213-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="44213-108">เนื่องจาก Nancy ทำงานในโครงการที่ต่างกันสองโครงการเมื่อเธออยู่ในแฟรงค์เฟิร์ต เมื่อเธอป้อนรายงานค่าใช้จ่ายของเธอ เธอได้กระจายค่าใช้จ่ายของเธอตามความเหมาะสมสำหรับแต่ละโครงการ</span><span class="sxs-lookup"><span data-stu-id="44213-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="44213-109">ตารางต่อไปนี้แสดงวิธีที่ Nancy กระจายค่าใช้จ่ายของเธอ</span><span class="sxs-lookup"><span data-stu-id="44213-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="44213-110">ชนิดของค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="44213-110">Expense type</span></span> | <span data-ttu-id="44213-111">รวมยอดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="44213-111">Total expense amount</span></span>|<span data-ttu-id="44213-112">ยอดเงินที่กระจายให้กับโครงการ A</span><span class="sxs-lookup"><span data-stu-id="44213-112">Amount distributed to project A</span></span>| <span data-ttu-id="44213-113">ยอดเงินที่กระจายให้กับโครงการ B</span><span class="sxs-lookup"><span data-stu-id="44213-113">Amount distributed to project B</span></span> |
|--------------|---------------------|-------------------------------|---------------------------------|
|<span data-ttu-id="44213-114">ค่าโดยสารรถไฟ</span><span class="sxs-lookup"><span data-stu-id="44213-114">Train fare</span></span>   |<span data-ttu-id="44213-115">578 โครเนอร์เดนมาร์ก</span><span class="sxs-lookup"><span data-stu-id="44213-115">DKK 578</span></span>              |<span data-ttu-id="44213-116">405 โครเนอร์เดนมาร์ก</span><span class="sxs-lookup"><span data-stu-id="44213-116">DKK 405</span></span>                        |<span data-ttu-id="44213-117">173 โครเนอร์เดนมาร์ก</span><span class="sxs-lookup"><span data-stu-id="44213-117">DKK 173</span></span>                          |
|<span data-ttu-id="44213-118">โรงแรม</span><span class="sxs-lookup"><span data-stu-id="44213-118">Hotel</span></span>         |<span data-ttu-id="44213-119">725 ยูโร</span><span class="sxs-lookup"><span data-stu-id="44213-119">EUR 725</span></span>              |<span data-ttu-id="44213-120">557 ยูโร</span><span class="sxs-lookup"><span data-stu-id="44213-120">EUR 557</span></span>                        |<span data-ttu-id="44213-121">168 ยูโร</span><span class="sxs-lookup"><span data-stu-id="44213-121">EUR 168</span></span>                          |
|<span data-ttu-id="44213-122">มื้ออาหาร</span><span class="sxs-lookup"><span data-stu-id="44213-122">Meals</span></span>         |<span data-ttu-id="44213-123">346 ยูโร</span><span class="sxs-lookup"><span data-stu-id="44213-123">EUR 346</span></span>              |<span data-ttu-id="44213-124">284 ยูโร</span><span class="sxs-lookup"><span data-stu-id="44213-124">EUR 284</span></span>                        |<span data-ttu-id="44213-125">62 ยูโร</span><span class="sxs-lookup"><span data-stu-id="44213-125">EUR 62</span></span>                           |

