---
title: สร้างลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ
description: หัวข้อนี้อธิบายเกี่ยวกับวิธีการสร้างลิงค์ที่กำหนดเองในการบริการตนเองของผู้จัดการใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4c9197ee124f53ff8d4acc90cb490113d35e80b4
ms.sourcegitcommit: 0c33864efdd66c6ac11a4f35d971c0bb4efb15db
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654300"
---
# <a name="create-custom-links-in-manager-self-service"></a><span data-ttu-id="7e044-103">สร้างลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="7e044-103">Create custom links in Manager self-service</span></span>

<span data-ttu-id="7e044-104">คุณสามารถเพิ่มลิงค์ที่กำหนดเองบนแท็บ **ทีมของฉัน** ในการบริการตนเองของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="7e044-104">You can add custom links on the **My team** tab in Manager self-service.</span></span> <span data-ttu-id="7e044-105">ลักษณะการทำงานนี้ช่วยให้คุณสามารถเข้าถึงข้อมูลที่สำคัญได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="7e044-105">This feature lets you provide quick access to important information.</span></span> <span data-ttu-id="7e044-106">มีความคล้ายคลึงกันกับการเพิ่มลิงค์ที่กำหนดเองในแท็บ **ข้อมูลของฉัน** ในการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="7e044-106">It's similar to adding custom links in the **My information** tab in Employee self service.</span></span>

## <a name="enable-the--feature"></a><span data-ttu-id="7e044-107">เปิดใช้งานคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="7e044-107">Enable the  feature</span></span>

<span data-ttu-id="7e044-108">เมื่อต้องการใช้คุณลักษณะนี้ ให้เปิดใช้งาน **ลิงค์ที่กำหนดเองในการบริการตนเองของผู้จัดการ** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="7e044-108">To use this feature, enable **Custom links in Manager self-service** in the **Feature management** workspace.</span></span> <span data-ttu-id="7e044-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะรุ่นพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="7e044-109">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="set-up-custom-links"></a><span data-ttu-id="7e044-110">ตั้งค่าการเชื่อมโยงแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7e044-110">Set up custom links</span></span>

1. <span data-ttu-id="7e044-111">ใน **พารามิเตอร์ทรัพยากรบุคคล** ให้เลือก **การบริการตนเองของผู้จัดการ**</span><span class="sxs-lookup"><span data-stu-id="7e044-111">In **Human Resources parameters**, select **Manager self service**.</span></span>

2. <span data-ttu-id="7e044-112">ภายใต้ **ตั้งค่าลิงค์สำหรับผู้จัดการ** คุณสามารถเพิ่ม แก้ไข หรือลบลิงค์ได้</span><span class="sxs-lookup"><span data-stu-id="7e044-112">Under **Set up links for Managers**, you can add, edit, or remove a link.</span></span> <span data-ttu-id="7e044-113">นอกจากนี้คุณยังสามารถจัดกลุ่มลิงค์เข้าด้วยกัน เพื่อให้แสดงผลในกลุ่มในการบริการตนเองของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="7e044-113">You can also group the links together so they display in a group in Manager self-service.</span></span>

   ![ตั้งค่าลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ](./media/hr-employee-manager-self-service-custom-links-setup.png)

3. <span data-ttu-id="7e044-115">เมื่อต้องการดูลิงค์ ให้ไปที่แท็บ **ทีมงานของฉัน** ในระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="7e044-115">To see the links, go to the **My team** tab in Employee self-service.</span></span>

   ![ดูลิงก์แบบกำหนดเองในระบบบริการตนเองของผู้จัดการ](./media/hr-employee-manager-self-service-custom-links-view.png)

## <a name="see-also"></a><span data-ttu-id="7e044-117">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="7e044-117">See also</span></span>

[<span data-ttu-id="7e044-118">ภาพรวมของระบบบริการตนเองของพนักงานและผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="7e044-118">Employee and Manager self-service overview</span></span>](hr-employee-manager-self-service-overview.md)
