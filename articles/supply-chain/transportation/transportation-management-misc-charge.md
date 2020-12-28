---
title: ค่าธรรมเนียมเบ็ดเตล็ดสำหรับการจัดการการขนส่ง
description: หัวข้อนี้อธิบายถึงวิธีการที่ต้องเชื่อมโยงค่าธรรมเนียมการขนส่งกับรหัสค่าธรรมเนียม
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438953"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="ddf71-103">ค่าธรรมเนียมเบ็ดเตล็ดสำหรับการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="ddf71-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddf71-104">ตามด้วยค่าธรรมเนียมเบ็ดเตล็ดทั้งหมด ค่าธรรมเนียมการขนส่งต้องเชื่อมโยงกับรหัสค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="ddf71-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="ddf71-105">มิฉะนั้น จะไม่มีการเพิ่มกลับไปยังใบสั่งเป็นค่าธรรมเนียมเบ็ดเตล็ด</span><span class="sxs-lookup"><span data-stu-id="ddf71-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="ddf71-106">**รหัสค่าธรรมเนียม** จะกำหนดวิธีการลงรายการบัญชีค่าธรรมเนียมสัมพันธ์กับใบสั่งและรายการใบสั่งที่มีการเพิ่มค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="ddf71-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="ddf71-107">ไปที่ **การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ค่าธรรมเนียมเบ็ดเตล็ด** เพื่อกำหนดเกณฑ์การกำหนดคุณสมบัติที่กำหนดเมื่อมีการใช้ **รหัสค่าธรรมเนียม** เฉพาะกับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="ddf71-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="ddf71-108">คุณควรติดตั้งอย่างน้อยหนึ่งรายการสำหรับแต่ละการตั้งค่า **โมดูลค่าธรรมเนียม** ที่เกี่ยวข้อง (*ลูกค้า* และ *ผู้จัดจำหน่าย*) ที่มีการตั้งค่า **ชนิดค่าธรรมเนียมเบ็ดเตล็ด** เป็น *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="ddf71-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="ddf71-109">ถ้าขาดหายไป ค่าธรรมเนียมเบ็ดเตล็ดจะ *ไม่* เพิ่มลงในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ddf71-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
