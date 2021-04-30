---
title: จัดการบทบาทผู้ใช้ใน Microsoft Teams
description: หัวข้อนี้อธิบายวิธีจัดการบทบาทผู้ใช้ Microsoft Dynamics 365 Commerce ใน Microsoft Teams.
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
ms.openlocfilehash: 53cdd1966e76dfcfc427e73520a680a610667617
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908817"
---
# <a name="manage-user-roles-in-microsoft-teams"></a><span data-ttu-id="7dbc8-103">จัดการบทบาทผู้ใช้ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7dbc8-103">Manage user roles in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7dbc8-104">หัวข้อนี้อธิบายวิธีจัดการบทบาทผู้ใช้ Microsoft Dynamics 365 Commerce ใน Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7dbc8-104">This topic describes how to manage Microsoft Dynamics 365 Commerce user roles in Microsoft Teams.</span></span>

<span data-ttu-id="7dbc8-105">เมื่อคุณสร้างทีมงานให้กับร้านค้าหรือช่องทางแต่ละแห่งใน Teams สมาชิกกลุ่มที่ตรงกับทีมงานจะถูกสร้างขึ้น (ตัวอย่างเช่น `HOUSTON_D365@<YourTenantAzureADDomain>.com`)</span><span class="sxs-lookup"><span data-stu-id="7dbc8-105">As you create a team for each store or channel in Teams, a group membership that corresponds to the team is created (for example, `HOUSTON_D365@<YourTenantAzureADDomain>.com`).</span></span> <span data-ttu-id="7dbc8-106">ผู้ปฏิบัติงานร้านค้าทั้งหมดภายใต้การเป็นสมาชิกกลุ่มทีมงานจะได้รับการมอบหมายบทบาทผู้ใช้อย่างใดอย่างหนึ่งจากสองบทบาท: **เจ้าของ** หรือ **สมาชิก**</span><span class="sxs-lookup"><span data-stu-id="7dbc8-106">All the store workers under a team group membership are assigned one of two user roles: **Owner** or **Member**.</span></span> <span data-ttu-id="7dbc8-107">จัดเก็บพนักงานที่มีบทบาทผู้ใช้ **เจ้าของ** สามารถดําเนินการได้ เช่น การเพิ่มช่องทางส่วนตัว และเพิ่มหรือลบสมาชิก</span><span class="sxs-lookup"><span data-stu-id="7dbc8-107">Store employees who have the **Owner** user role can perform operations such as adding a private channel, and adding or deleting members.</span></span> <span data-ttu-id="7dbc8-108">โดยทั่วไป ผู้จัดการร้านค้าจะมีบทบาทผู้ใช้ **เจ้าของ**</span><span class="sxs-lookup"><span data-stu-id="7dbc8-108">Typically, store managers have the **Owner** user role.</span></span>

<span data-ttu-id="7dbc8-109">ภาพประกอบต่อไปนี้จะแสดงตัวอย่างของรายชื่อสมาชิกทีมงานและบทบาทผู้ใช้ของสมาชิกในศูนย์การจัดการ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7dbc8-109">The following illustration shows an example of a list of team members and their user roles in the Microsoft Teams admin center.</span></span>

![สมาชิกทีมงานและบทบาทผู้ใช้ในศูนย์การจัดการ Microsoft Teams](media/d365-commerce-teams-integration-user-roles.png)

<span data-ttu-id="7dbc8-111">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [กําหนดเจ้าของทีมงานและสมาชิกใน Microsoft Teams](https://docs.microsoft.com/microsoftteams/assign-roles-permissions)</span><span class="sxs-lookup"><span data-stu-id="7dbc8-111">For more information, see [Assign team owners and members in Microsoft Teams](https://docs.microsoft.com/microsoftteams/assign-roles-permissions).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dbc8-112">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7dbc8-112">Additional resources</span></span>

[<span data-ttu-id="7dbc8-113">ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7dbc8-113">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="7dbc8-114">เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7dbc8-114">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="7dbc8-115">สํารอง Microsoft Teams จาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7dbc8-115">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="7dbc8-116">ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="7dbc8-116">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="7dbc8-117">แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7dbc8-117">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="7dbc8-118">คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7dbc8-118">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
