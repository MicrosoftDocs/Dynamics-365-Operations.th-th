---
title: งานไม่ถูกบล็อค
description: งานไม่ถูกบล็อค
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924215"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="c34ab-103">งานไม่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="c34ab-103">Work isn't blocked</span></span>

<span data-ttu-id="c34ab-104">รหัสข้อผิดพลาด: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="c34ab-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="c34ab-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="c34ab-105">Symptoms</span></span>

<span data-ttu-id="c34ab-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c34ab-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c34ab-107">ไม่ได้บล็อคงานที่มีรหัส %1</span><span class="sxs-lookup"><span data-stu-id="c34ab-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="c34ab-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="c34ab-108">Cause</span></span>

<span data-ttu-id="c34ab-109">ตัวเลือก **เวฟที่บล็อค** ในเวฟถูกตั้งค่าเป็น *ไม่*</span><span class="sxs-lookup"><span data-stu-id="c34ab-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="c34ab-110">ไม่สามารถยกเลิกการบล็อคงานเนื่องจากไม่ได้บล็อคอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="c34ab-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="c34ab-111">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="c34ab-111">Resolution</span></span>

 <span data-ttu-id="c34ab-112">เฉพาะงานที่ตั้งค่าตัวเลือก **เวฟที่บล็อค** เป็น *ใช่* เท่านั้นที่สามารถถูกบล็อคได้</span><span class="sxs-lookup"><span data-stu-id="c34ab-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
