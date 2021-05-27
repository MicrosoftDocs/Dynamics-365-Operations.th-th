---
title: คุณไม่สามารถอัปเดตต้นทุนต่อหน่วยที่คาดการณ์เมื่อคุณนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ
description: เมื่อคุณใช้เอนทิตีข้อมูลเพื่อนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ ราคาต้นทุนของเรกคอร์ดที่มีอยู่จะไม่อัปเดตเพื่อให้ตรงกับข้อมูลที่นําเข้า
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026953"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="e67b8-103">คุณไม่สามารถอัปเดตต้นทุนต่อหน่วยที่คาดการณ์เมื่อคุณนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="e67b8-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="e67b8-104">หมายเลข KB: 4614109</span><span class="sxs-lookup"><span data-stu-id="e67b8-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="e67b8-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="e67b8-105">Symptoms</span></span>

<span data-ttu-id="e67b8-106">เมื่อคุณใช้เอนทิตีข้อมูลเพื่อนําเข้าเรกคอร์ดการคาดการณ์ความต้องการ ค่า **ต้นทุนต่อหน่วยที่คาดการณ์** ของเรกคอร์ดที่มีอยู่จะไม่อัปเดตเพื่อให้ตรงกับข้อมูลที่นําเข้า</span><span class="sxs-lookup"><span data-stu-id="e67b8-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="e67b8-107">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="e67b8-107">Cause</span></span>

<span data-ttu-id="e67b8-108">**ต้นทุนต่อหน่วยที่คาดการณ์** เป็นฟิลด์อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="e67b8-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="e67b8-109">ค่าขึ้นอยู่กับต้นทุนต่อหน่วยผลิตภัณฑ์และไม่สามารถตั้งค่าโดยตรงผ่านการนําเข้า</span><span class="sxs-lookup"><span data-stu-id="e67b8-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="e67b8-110">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="e67b8-110">Resolution</span></span>

<span data-ttu-id="e67b8-111">เนื่องจากฟิลด์เป็นแบบอ่านอย่างเดียว คุณจึงไม่สามารถนําเข้าค่าได้</span><span class="sxs-lookup"><span data-stu-id="e67b8-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="e67b8-112">ค่านี้จะคํานวณตามตรรกะทางธุรกิจที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="e67b8-112">The value will be calculated according to the existing business logic.</span></span>
