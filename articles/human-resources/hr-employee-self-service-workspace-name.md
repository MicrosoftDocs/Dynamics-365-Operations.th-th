---
title: เปลี่ยนพื้นที่ทำงานของระบบบริการตนเองของลูกค้า
description: หัวข้อนี้จะอธิบายวิธีการเปลี่ยนชื่อที่แสดงของพื้นที่ทำงานของระบบบริการตนเองของพนักงานใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 07/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51adcb2c06044b030ce3b96f0c71129e8c0acd8c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790679"
---
# <a name="change-employee-self-service-workspace-name"></a><span data-ttu-id="3bf01-103">เปลี่ยนพื้นที่ทำงานของระบบบริการตนเองของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3bf01-103">Change Employee self service workspace name</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3bf01-104">ถ้าคุณมีอาสาสมัครหรือผู้อื่นที่ไม่ใช่พนักงาน คุณอาจต้องการเปลี่ยนชื่อของพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="3bf01-104">If you have volunteers or other non-employees, you might want to change the name of the **Employee self-service** workspace.</span></span> <span data-ttu-id="3bf01-105">คุณสามารถเปลี่ยนพื้นที่ทำงานนี้เป็น **ระบบบริการตนเอง** แทน</span><span class="sxs-lookup"><span data-stu-id="3bf01-105">You can change this workspace to **Self service** instead.</span></span>

> [!NOTE]
> <span data-ttu-id="3bf01-106">การเปลี่ยนชื่อของพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน** ยังเปลี่ยนรายการเมนูที่ใช้ภายในโดย Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="3bf01-106">Changing the name of the **Employee self-service** workspace also changes the menu item that is used internally by Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3bf01-107">ถ้าคุณใช้การเลือกกำหนดความปลอดภัยก่อนหน้านี้กับรายการเมนู **HcmEmployeeSelfServiceWorkspace** เราขอแนะนำให้ใช้การเปลี่ยนแปลงเดียวกันกับ **HcmSelfServiceWorkspace** เพื่อรักษาพาริตี้</span><span class="sxs-lookup"><span data-stu-id="3bf01-107">If you previously applied security customizations to the **HcmEmployeeSelfServiceWorkspace** menu item, we recommend applying the same changes to **HcmSelfServiceWorkspace** to maintain parity.</span></span>

1. <span data-ttu-id="3bf01-108">ในทรัพยากรบุคคล ให้เลือก **การจัดการบุคลากร** เลือก **ลิงค์** แล้วจากนั้น เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="3bf01-108">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

2. <span data-ttu-id="3bf01-109">เลือกแท็บ **ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="3bf01-109">Select the **Employee self-service** tab.</span></span>

3. <span data-ttu-id="3bf01-110">ภายใต้ **ชื่อที่แสดง** ให้เลือก **ระบบบริการตนเอง**</span><span class="sxs-lookup"><span data-stu-id="3bf01-110">Under **Display name**, select **Self service**.</span></span>

   ![เปลี่ยนชื่อพื้นที่ทำงานของระบบบริการตนเองของลูกค้าเป็นระบบบริการตนเอง](./media/hr-employee-self-service-workspace-name.png)

4. <span data-ttu-id="3bf01-112">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3bf01-112">Select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3bf01-113">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3bf01-113">Additional resources</span></span>

- [<span data-ttu-id="3bf01-114">ภาพรวมของระบบบริการตนเองของพนักงานและผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="3bf01-114">Employee and Manager self-service overview</span></span>](hr-employee-manager-self-service-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]