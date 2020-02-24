---
title: สร้างลำดับงานคำขอลางาน
description: สร้างลำดับงานคำขอลางานและขาดงานเพื่อจัดการคำขอในการลาอย่างสม่ำเสมอใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2689a0cdf2969455a301593e8f60b10c07e6f91
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010712"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="389bc-103">สร้างลำดับงานคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="389bc-103">Create a leave request workflow</span></span>

<span data-ttu-id="389bc-104">คุณสามารถสร้างลำดับงานใน Dynamics 365 Human Resources เพื่อจัดการคำขอลางานและขาดงานอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="389bc-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="389bc-105">ลำดับงาน **การลางานและการขาดงาน** ช่วยให้คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="389bc-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="389bc-106">กำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="389bc-106">Define tasks</span></span>
- <span data-ttu-id="389bc-107">กำหนดว่าใครต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="389bc-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="389bc-108">ระบุว่าใครสามารถอนุมัติหรือปฏิเสธคำขอได้</span><span class="sxs-lookup"><span data-stu-id="389bc-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="389bc-109">สร้างลำดับงานคำขอลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="389bc-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="389bc-110">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="389bc-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="389bc-111">ภายใต้ **ตั้งค่า** โปรดเลือก **ลำดับงานของฝ่ายทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="389bc-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="389bc-112">โปรดเลือก **สร้าง** แล้วเลือก **คำขอลางานและขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="389bc-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="389bc-113">เมื่อกล่องข้อความ **เปิดไฟล์นี้หรือไม่** ปรากฏขึ้น โปรดเลือก **เปิด** และล็อกอินด้วยข้อมูลประจำตัวของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="389bc-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="389bc-114">ใช้โปรแกรมแก้ไขลำดับงานเพื่อสร้างลำดับงานสำหรับคำขอลางานของคุณ</span><span class="sxs-lookup"><span data-stu-id="389bc-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="389bc-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการทำงานกับลำดับงาน โปรดดูที่ [ภาพรวมของการสร้างลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="389bc-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="see-also"></a><span data-ttu-id="389bc-116">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="389bc-116">See also</span></span>

- [<span data-ttu-id="389bc-117">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="389bc-117">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)