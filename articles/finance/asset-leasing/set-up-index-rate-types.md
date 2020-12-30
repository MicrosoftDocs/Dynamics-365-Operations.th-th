---
title: ตั้งค่าอัตราดัชนี
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าอัตราดัชนี ต้องระบุอัตราดัชนีถ้าองค์กรของคุณเชื่อมโยงยอดเงินการชำระค่าเช่ากับชุดของอัตราดัชนี
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16b83102aa76f46473138f89ea487e71668a188c
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4448607"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="e0e84-104">ตั้งค่าอัตราดัชนี</span><span class="sxs-lookup"><span data-stu-id="e0e84-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0e84-105">ถ้าการชำระค่าเช่าขึ้นอยู่กับดัชนี คุณสามารถเพิ่มและรักษาชนิดอัตราดัชนีในระบบได้</span><span class="sxs-lookup"><span data-stu-id="e0e84-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="e0e84-106">เมื่อต้องการกำหนดค่าการชำระค่าเช่าใหม่จากหน้า **ชนิดอัตราดัชนี** กระบวนการประเมินค่าใหม่ของอัตราดัชนีจะใช้อัตราดัชนีล่าสุดจากวันที่ประเมินค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="e0e84-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="e0e84-107">เมื่อต้องการเพิ่มชนิดอัตราดัชนีและอัตราดัชนี ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e0e84-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="e0e84-108">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> ชนิดอัตราดัชนี**</span><span class="sxs-lookup"><span data-stu-id="e0e84-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="e0e84-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e0e84-109">Select **New**.</span></span>
3. <span data-ttu-id="e0e84-110">ในฟิลด์ที่เหมาะสม ให้ป้อนชนิดอัตราและชื่อของอัตราดัชนี</span><span class="sxs-lookup"><span data-stu-id="e0e84-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="e0e84-111">เมื่อต้องการเพิ่มค่าอัตราดัชนีใหม่ ให้เลือกชนิดอัตราดัชนี แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="e0e84-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="e0e84-112">เลือกวันที่เริ่มต้นที่มีผลบังคับใช้ของอัตรา และเลือกมูลค่าอัตรา</span><span class="sxs-lookup"><span data-stu-id="e0e84-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="e0e84-113">คุณต้องเลือก **ความแตกต่างของค่าอัตราดัชนี** หรือ **ค่าอัตราดัชนี** เป็นวิธีการอัตราดัชนี</span><span class="sxs-lookup"><span data-stu-id="e0e84-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="e0e84-114">เลือกวิธีการ **ความแตกต่างของมูลค่าอัตราดัชนี** เพื่อคำนวณการชำระค่าเช่าใหม่ ตามผลต่างระหว่างอัตราดัชนีในวันที่เริ่มต้นและอัตราดัชนีล่าสุด</span><span class="sxs-lookup"><span data-stu-id="e0e84-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="e0e84-115">มีการกำหนดอัตราดัชนีในฟิลด์ **อัตราดัชนี (%)**</span><span class="sxs-lookup"><span data-stu-id="e0e84-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="e0e84-116">เลือกวิธีการ **ค่าอัตราดัชนี** เพื่อคำนวณการชำระค่าเช่าโดยใช้เปอร์เซ็นต์ที่ระบุไว้ในฟิลด์ **อัตราดัชนี (%)**</span><span class="sxs-lookup"><span data-stu-id="e0e84-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>
