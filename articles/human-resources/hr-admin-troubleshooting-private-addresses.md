---
title: เข้าถึงที่อยู่ส่วนตัวตามบทบาทความปลอดภัย
description: บทความนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งลูกค้าไม่สามารถเข้าถึงที่อยู่ส่วนตัวได้
author: andreabichsel
manager: tfehr
ms.date: 11/02/2018
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49f9f50b774df8e215c084bbb493a6be9de6b234
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463947"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="ee159-103">เข้าถึงที่อยู่ส่วนตัวตามบทบาทความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="ee159-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ee159-104">**ออก**</span><span class="sxs-lookup"><span data-stu-id="ee159-104">**Issue**</span></span>

<span data-ttu-id="ee159-105">หลังจากที่ลูกค้าทำซ้ำบทบาทความปลอดภัยและลงชื่อเข้าใช้ในฐานะบทบาทใหม่นั้น ลูกค้าไม่สามารถดูที่อยู่ที่ถูกทำเครื่องหมายเป็นส่วนตัวได้</span><span class="sxs-lookup"><span data-stu-id="ee159-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="ee159-106">**การแก้ปัญหา**</span><span class="sxs-lookup"><span data-stu-id="ee159-106">**Resolution**</span></span>

<span data-ttu-id="ee159-107">เพื่อแก้ปัญหา ลูกค้าต้องทำตามขั้นตอนเหล่านี้สำหรับบทบาทความปลอดภัยที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="ee159-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="ee159-108">ไปที่ **การจัดการองค์กร \> สมุดที่อยู่สากล \> พารามิเตอร์ของสมุดที่อยู่สากล**</span><span class="sxs-lookup"><span data-stu-id="ee159-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="ee159-109">บนแท็บ **ความปลอดภัยที่ตั้งส่วนตัว** ย้ายบทบาทความปลอดภัยใหม่จากรายการ **บทบาทที่พร้อมใช้งาน** ไปยังรายการ **บทบาทที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="ee159-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="ee159-110">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ee159-110">Select **Save**.</span></span>

![พารามิเตอร์สมุดที่อยู่สากล](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]