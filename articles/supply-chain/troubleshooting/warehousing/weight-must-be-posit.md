---
title: น้ำหนักต้องเป็นค่าบวก
description: น้ำหนักต้องเป็นค่าบวก
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924314"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="1a305-103">น้ำหนักต้องเป็นค่าบวก</span><span class="sxs-lookup"><span data-stu-id="1a305-103">Weight must be positive</span></span>

<span data-ttu-id="1a305-104">รหัสข้อผิดพลาด: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="1a305-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="1a305-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="1a305-105">Symptoms</span></span>

<span data-ttu-id="1a305-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a305-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1a305-107">น้ำหนักต้องเป็นค่าบวก</span><span class="sxs-lookup"><span data-stu-id="1a305-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="1a305-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="1a305-108">Cause</span></span>

<span data-ttu-id="1a305-109">ฟิลด์ **น้ําหนักรวม** จะถูกตั้งค่าเป็น *0* (ศูนย์) หรือค่าลบ</span><span class="sxs-lookup"><span data-stu-id="1a305-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="1a305-110">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="1a305-110">Resolution</span></span>

<span data-ttu-id="1a305-111">เมื่อต้องการระบุน้ำหนัก ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="1a305-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="1a305-112">ในฟิลด์ **น้ําหนักรวม** ให้ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="1a305-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="1a305-113">จากนั้นเลือกหน่วยในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="1a305-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="1a305-114">เลือก **ดูน้ําหนักของระบบ** เพื่อคํานวณค่า **น้ําหนักรวม**</span><span class="sxs-lookup"><span data-stu-id="1a305-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
