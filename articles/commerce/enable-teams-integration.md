---
title: เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams
description: หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4d596f27ffe15a97dc04e2ce7e85d21f8e7161f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908406"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="f7298-103">เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7298-104">หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="f7298-105">เมื่อต้องการเตรียมใช้งาน Teams ด้วยข้อมูลจาก Dynamics 365 Commerce และซิงโครไนส์ลักษณะการงานการจัดการงานระหว่าง Teams และโปรแกรมประยุกต์การขายหน้าร้าน (POS) คุณต้องเปิดใช้งานคุณลักษณะการรวมในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="f7298-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="f7298-106">เมื่อคุณเปิดใช้งานการรวม Teams คุณยินยอมให้แบ่งปันข้อมูลของคุณกับ Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="f7298-107">ข้อมูลที่ใช้ร่วมกันกับ Teams อาจอยู่ในประเทศอื่นที่แตกต่างจากข้อมูล Commerce ของคุณ และอาจขึ้นอยู่กับมาตรฐานการปฏิบัติตามกฎระเบียบที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f7298-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="f7298-108">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ศูนย์ความเชื่อถือของ Microsoft](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="f7298-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="f7298-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับนโยบายสิทธิส่วนบุคคลของ Microsoft โปรดดูที่ [รายงานสิทธิส่วนบุคคลของ Microsoft](https://aka.ms/privacy)</span><span class="sxs-lookup"><span data-stu-id="f7298-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="f7298-110">เปิดใช้งานการรวม Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-110">Enable Teams integration</span></span>

<span data-ttu-id="f7298-111">ก่อนที่คุณจะสามารถเปิดใช้งานการรวม Microsoft Teams กับ Commerce ได้ คุณต้องลงทะเบียนโปรแกรมประยุกต์ Teams กับผู้เช่าของคุณในพอร์ทัล Azure ก่อน</span><span class="sxs-lookup"><span data-stu-id="f7298-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="f7298-112">หากต้องการลงทะเบียนโปรแกรมประยุกต์ Teams กับผู้เช่าในพอร์ทัล Azure ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7298-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="f7298-113">ปฏิบัติตามขั้นตอนใน [เริ่มต้นใช้งานด่วน: ลงทะเบียนแอปในแพลตฟอร์มเอกลักษณ์ Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) เพื่อลงทะเบียนโปรแกรมประยุกต์ Teams กับผู้เช่าในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="f7298-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="f7298-114">คัดลอก **ค่ารหัสโปรแกรมประยุกต์ (ไคลเอนต์)** จากหน้า **ภาพรวม** ของแอปที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7298-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="f7298-115">คุณจะใช้ค่านี้เปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="f7298-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="f7298-116">คัดลอกค่าใบรับรองที่ป้อนเมื่อคุณ [เพิ่มใบรับรอง](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) ในขั้นตอนที่ 1</span><span class="sxs-lookup"><span data-stu-id="f7298-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="f7298-117">ใบรับรองเรียกอีกอย่างว่าคีย์สาธารณะหรือคีย์โปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="f7298-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="f7298-118">คุณจะใช้ค่านี้เปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="f7298-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="f7298-119">เมื่อต้องการเปิดใช้งานการรวม Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7298-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f7298-120">ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**</span><span class="sxs-lookup"><span data-stu-id="f7298-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="f7298-121">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f7298-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f7298-122">ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Microsoft Teams** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="f7298-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="f7298-123">ในฟิลด์ **รหัสโปรแกรมประยุกต์** และ **คีย์โปรแกรมประยุกต์** ให้ป้อนค่าที่คุณได้รับเมื่อคุณลงทะเบียนโปรแกรมประยุกต์ Teams ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="f7298-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="f7298-124">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f7298-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="f7298-125">ภาพต่อไปนี้แสดงตัวอย่างการตั้งค่าคอนฟิกการรวม Teams ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="f7298-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![การตั้งค่าคอนฟิกการรวม Teams ในศูนย์ควบคุม Commerce](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="f7298-127">ปิดใช้งานการรวม Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-127">Disable Teams integration</span></span>

<span data-ttu-id="f7298-128">เมื่อต้องการปิดใช้งานการรวม Microsoft Teams ในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7298-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f7298-129">ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่าคอนฟิกการรวม Microsoft Teams**</span><span class="sxs-lookup"><span data-stu-id="f7298-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="f7298-130">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f7298-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="f7298-131">ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Microsoft Teams** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="f7298-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="f7298-132">ล้างข้อมูลค่าออกจากฟิลด์ **รหัสโปรแกรมประยุกต์** และ **คีย์โปรแกรมประยุกต์**</span><span class="sxs-lookup"><span data-stu-id="f7298-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="f7298-133">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f7298-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f7298-134">หลังจากที่คุณปิดใช้งานการรวม Teams กับ Commerce แล้ว เทอร์มินัล POS จะไม่แสดงงานที่เผยแพร่จากโปรแกรมประยุกต์ Teams อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="f7298-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7298-135">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f7298-135">Additional resources</span></span>

[<span data-ttu-id="f7298-136">ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="f7298-137">สํารอง Microsoft Teams จาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f7298-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="f7298-138">ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="f7298-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="f7298-139">จัดการบทบาทผู้ใช้ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="f7298-140">แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="f7298-141">คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f7298-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
