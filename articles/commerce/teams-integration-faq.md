---
title: คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams
description: หัวข้อนี้มีข้อมูลเกี่ยวกับคำตอบสำหรับคำถามที่ถามบ่อยเกี่ยวกับการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams
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
ms.openlocfilehash: bf9aebb1c8ba7cf4fee3f0471a10872de1e23ce6
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908867"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="ba240-103">คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba240-104">หัวข้อนี้มีข้อมูลเกี่ยวกับคำตอบสำหรับคำถามที่ถามบ่อยเกี่ยวกับการรวม Microsoft Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="ba240-105">ใครในร้านค้าจะกลายเป็นเจ้าของทีมงานขณะเตรียมใช้งาน Teams จาก Commerce</span><span class="sxs-lookup"><span data-stu-id="ba240-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="ba240-106">ผู้จัดการร้านค้าทั้งหมดจะถูกเพิ่มเป็นเจ้าของกลุ่มทีมงานที่ตรงกันโดยอัตโนมัติ เพื่อให้สามารถดําเนินการได้ เช่น การเพิ่มช่องทางส่วนตัวและเพิ่มหรือลบสมาชิก</span><span class="sxs-lookup"><span data-stu-id="ba240-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="ba240-107">ฉันจะกําหนดบทบาท "ผู้จัดการฝ่ายสื่อสาร" ให้กับพนักงานในศูนย์ควบคุม Commerce อย่างไร</span><span class="sxs-lookup"><span data-stu-id="ba240-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="ba240-108">ผู้จัดการฝ่ายการสื่อสาร Microsoft Teams สามารถสร้างและเผยแพร่รายการงานได้</span><span class="sxs-lookup"><span data-stu-id="ba240-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="ba240-109">พนักงานในองค์กรที่ต้องเป็นผู้จัดการการสื่อสารต้องมีบทบาทเป็น "ผู้จัดการฝ่ายงานขายปลีก" ที่มอบหมายให้กับพนักงานในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="ba240-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="ba240-110">เมื่อต้องการกําหนดบทบาทผู้จัดการงานขายปลีกให้กับพนักงานในศูนย์ควบคุม Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba240-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ba240-111">ไปยัง **การขายปลีกและการค้า \> พนักงาน \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ba240-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="ba240-112">เลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="ba240-112">Select an employee.</span></span>
1. <span data-ttu-id="ba240-113">บนแท็บด่วน **บทบาทของผู้ใช้** ให้เลือก **กำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="ba240-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="ba240-114">ในกล่องโต้ตอบ **กำหนดบทบาทให้กับผู้ใช้** ให้เลือกบทบาทของ **ผู้จัดการงานขายปลีก** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba240-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="ba240-115">ฉันจะสามารถอัพโหลดลำดับชั้นขององค์กรเป็นลำชั้นขององค์กรเฉพาะ Microsoft Teams ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="ba240-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="ba240-116">ในศูนย์ควบคุม Commerce ลำดับชั้นขององค์กรทั้งหมดจะเชื่อมโยงกับวัตถุประสงค์หนึ่งวัตถุประสงค์หรือมากกว่า</span><span class="sxs-lookup"><span data-stu-id="ba240-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="ba240-117">ตรวจสอบให้แน่ใจว่าลำดับชั้นที่คุณต้องการเตรียมใช้งาน Microsoft Teams มีวัตถุประสงค์ **การรายงานการขายปลีก** ที่เชื่อมโยงอยู่ด้วย ดังที่แสดงในรูปภาพตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba240-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![ตัวอย่างของวัตถุประสงค์ของลำดับชั้นขององค์กรขององค์กรในศูนย์ควบคุม Commerce](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="ba240-119">ฉันจะเปิดใช้งานผู้ปฏิบัติงานของร้านค้าปลีกเพื่อล็อกอินเข้าสู่การขายหน้าร้านของ Commerce (POS) โดยใช้ Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="ba240-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="ba240-120">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีตั้งค่าคอนฟิกประสบการณ์การลงชื่อเข้าใช้ Commerce POS เพื่อใช้การรับรองความถูกต้อง Azure AD โปรดดูที่ [เปิดใช้งานการรับรองความถูกต้อง Azure Active Directory ของการลงชื่อเข้าใช้ POS](aad-pos-logon.md)</span><span class="sxs-lookup"><span data-stu-id="ba240-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="ba240-121">ฉันจะแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce ได้อย่างไร ถ้าองค์กรได้สร้างทีมงานไว้แล้วใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="ba240-122">หากต้องการข้อมูลเกี่ยวกับวิธีการแม็ปร้านค้าและทีมงานหากมีทีมงานที่มีอยู่แล้ว โปรดดูที่ [แม็ปร้านค้าและทีมงานที่ตรงกันหากองค์กรของคุณมีทีมงานที่มีอยู่ก่อนอยู่แล้วใน Microsoft Teams](map-stores-existing-teams.md)</span><span class="sxs-lookup"><span data-stu-id="ba240-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="ba240-123">ฉันจะล้างข้อมูลโทเคน Microsoft Graph API ที่จัดเก็บไว้ในที่จัดเก็บรอบเวลาอย่างไร</span><span class="sxs-lookup"><span data-stu-id="ba240-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="ba240-124">ผู้ใช้ที่ลงชื่อเข้าใช้การขายหน้าร้าน (POS) ที่มีบัญชี Azure Active Directory (Azure AD) ควรลงชื่อออกจาก POS หรือปิดโปรแกรมประยุกต์เพื่อล้างข้อมูลการจัดเก็บรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="ba240-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="ba240-125">แนวทางที่แนะนาคือต้องมีผู้ปฏิบัติงานของร้านค้าล็อคเทอร์มินัล POS หรือออกจากรอบเวลาเสมอเมื่อไม่ใช้เทอร์มินัล</span><span class="sxs-lookup"><span data-stu-id="ba240-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="ba240-126">เกิดอะไรขึ้นถ้าร้านค้าไม่มีผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="ba240-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="ba240-127">หากร้านค้าไม่มีผู้จัดการ ระบบจะไม่สร้างกลุ่มทีมงานให้กับร้านค้าหรือใน Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="ba240-128">เกิดอะไรขึ้นถ้าผู้จัดการร้านค้าลาออกจากบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba240-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="ba240-129">ผู้ที่มีบทบาทเจ้าของสามารถเพิ่มผู้จัดการร้านค้าใหม่ในศูนย์ควบคุม Commerce และ Teams เตรียมใช้งานใหม่เพื่อให้ผู้จัดการใหม่มีสิทธิ์ที่จําเป็นใน Teams ของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="ba240-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ba240-130">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ba240-130">Additional resources</span></span>

[<span data-ttu-id="ba240-131">ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ba240-132">เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ba240-133">สํารอง Microsoft Teams จาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ba240-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ba240-134">ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="ba240-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ba240-135">จัดการบทบาทผู้ใช้ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ba240-136">แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba240-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
