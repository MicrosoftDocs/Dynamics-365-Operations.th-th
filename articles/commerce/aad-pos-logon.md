---
title: เปิดใช้งานการรับรองความถูกต้อง Azure Active Directory สำหรับการลงชื่อเข้าใช้ POS
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกประสบการณ์ในการลงชื่อเข้าใช้สำหรับการขายหน้าร้าน (POS) ของ Microsoft Dynamics 365 Commerce เพื่อใช้ในการรับรองความถูกต้อง Azure Active Directory
author: boycezhu
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 50088aee8c2474708682c9041251d2336e84d971
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796353"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="62294-103">เปิดใช้งานการรับรองความถูกต้อง Azure Active Directory สำหรับการลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="62294-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="62294-104">ลูกค้าหลายรายที่ใช้ Microsoft Dynamics 365 Commerce ยังใช้ Microsoft Cloud Service อื่นๆ และพวกเขาอาจใช้ Azure Active Directory (Azure AD) เพื่อจัดการข้อมูลประจำตัวของผู้ใช้สำหรับบริการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="62294-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="62294-105">ในกรณีดังกล่าว ลูกค้าอาจต้องการใช้บัญชี Azure AD เดียวกันระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="62294-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="62294-106">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกประสบการณ์ในการลงชื่อเข้าใช้สำหรับการขายหน้าร้าน (POS) ของ Commerce เพื่อให้ใช้การรับรองความถูกต้อง Azure AD</span><span class="sxs-lookup"><span data-stu-id="62294-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="62294-107">ตั้งค่าคอนฟิกการรับรองความถูกต้อง Azure AD</span><span class="sxs-lookup"><span data-stu-id="62294-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="62294-108">เมื่อต้องการทำให้ Azure AD พร้อมใช้งานเป็นวิธีการรับรองความถูกต้องสำหรับการลงชื่อเข้าใช้ POS สำหรับร้านค้า คุณต้องตั้งค่าคอนฟิกการตั้งค่าของโพรไฟล์ฟังก์ชันของร้านค้า แล้วใช้การตั้งค่าเหล่านั้นกับไคลเอนต์ POS</span><span class="sxs-lookup"><span data-stu-id="62294-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="62294-109">เมื่อต้องการตั้งค่าคอนฟิกโพรไฟล์ฟังก์ชัน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="62294-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="62294-110">ไปยัง **การขายปลีกและการค้า** \> **การตั้งค่าช่องทาง** \> **การตั้งค่า POS** \> **โปรไฟล์ POS** \> **โปรไฟล์ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="62294-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="62294-111">เลือกโพรไฟล์ฟังก์ชันที่จะเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="62294-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="62294-112">บน FastTab **ฟังก์ชัน** ในส่วน **การเข้าสู่ระบบของพนักงาน POS** ให้เปลี่ยนค่าของฟิลด์ **วิธีการรับรองความถูกต้องของการเข้าสู่ระบบ** จาก **รหัสบุคลากรและรหัสผ่าน** เป็น **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="62294-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="62294-113">โดยค่าเริ่มต้น โพรไฟล์ฟังก์ชันทั้งหมดจะใช้ **รหัสบุคลากรและรหัสผ่าน** เป็นวิธีการรับรองความถูกต้องของ POS</span><span class="sxs-lookup"><span data-stu-id="62294-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="62294-114">ดังนั้น คุณต้องเปลี่ยนค่าของฟิลด์ **วิธีการรับรองความถูกต้องของการเข้าสู่ระบบ** ถ้าคุณต้องการใช้ตรรกะ Azure AD</span><span class="sxs-lookup"><span data-stu-id="62294-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="62294-115">ร้านค้าปลีกทั้งหมดที่เชื่อมโยงกับโพรไฟล์ฟังก์ชันที่เลือกจะได้รับผลกระทบจากการเปลี่ยนแปลงนี้</span><span class="sxs-lookup"><span data-stu-id="62294-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="62294-116">เมื่อต้องการใช้การตั้งค่ากับไคลเอนต์ POS ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="62294-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="62294-117">ไปยัง **การขายปลีกและการค้า** \> **การขายปลีกและไอทีเชิงพาณิชย์** \> **กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="62294-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="62294-118">รันงาน **1070** (**การตั้งค่าคอนฟิกช่องทาง**) กำหนดการการกระจาย</span><span class="sxs-lookup"><span data-stu-id="62294-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="62294-119">การตรวจสอบความถูกต้อง Azure AD ต้องใช้การเชื่อมต่ออินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="62294-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="62294-120">การดำเนินการนี้จะไม่ทำงานเมื่อ POS อยู่ในโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="62294-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="62294-121">ในขณะนี้ฟังก์ชัน **การแทนที่ผู้จัดการ** ไม่สนับสนุน Azure AD เป็นวิธีการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="62294-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="62294-122">ต้องระบุรหัสผู้ปฏิบัติการและรหัสผ่านแม้ว่า Azure AD จะมีการตั้งค่าคอนฟิกเป็นวิธีการรับรองความถูกต้องสำหรับการลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="62294-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="62294-123">เชื่อมโยงบัญชี Azure AD กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="62294-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="62294-124">ก่อนที่ผู้ปฏิบัติงานร้านค้าจะสามารถใช้บัญชี Azure AD เพื่อลงชื่อเข้าใช้ไปยังแอพลิเคชัน POS ได้ บัญชี Azure AD ต้องเชื่อมโยงกับผู้ปฏิบัติงานนั้น</span><span class="sxs-lookup"><span data-stu-id="62294-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="62294-125">เมื่อต้องการเชื่อมโยงบัญชี Azure AD กับผู้ปฏิบัติงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="62294-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="62294-126">ไปยัง **Retail และ Commerce** \> **พนักงาน** \> **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="62294-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="62294-127">เปิดหน้ารายละเอียดสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="62294-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="62294-128">บนบานหน้าต่างการดำเนินการ บนแท็บ **Commerce** ในกลุ่ม **ข้อมูลเฉพาะตัวภายนอก** ให้เลือก **เชื่อมโยงข้อมูลเฉพาะตัวที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="62294-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="62294-129">ในกล่องโต้ตอบ **ใช้ข้อมูลเฉพาะตัวภายนอกที่มีอยู่** ให้เลือก **ค้นหาโดยใช้อีเมล** ป้อนที่อยู่อีเมล Azure AD แล้วเลือก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="62294-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="62294-130">เลือกบัญชี Azure AD ที่จะส่งคืน แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="62294-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="62294-131">ฟิลด์ **นามแฝง** **UPN** และ **ตัวระบุย่อยภายนอก** บนแท็บ **Commerce** ของหน้ารายละเอียดของผู้ปฏิบัติงานจะถูกกรอกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="62294-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="62294-132">หลังจากที่มีการอัพเดตเรกคอร์ดผู้ปฏิบัติงานแล้ว ตัวอย่างเช่น หากมีการเชื่อมโยง Azure AD กับบัญชีใหม่ รหัสผ่านมีการเปลี่ยนแปลงหรือมีการอัพเดตสมุดที่อยู่ของพนักงาน ขอแนะนำให้คุณรันกำหนดการกระจาย **1060** (**พนักงาน**) เพื่อซิงโครไนส์ข้อมูลพนักงานล่าสุดไปยังช่องทาง</span><span class="sxs-lookup"><span data-stu-id="62294-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="62294-133">ด้วยวิธีนี้ แอปพลิเคชัน POS สามารถดึงข้อมูลที่ถูกต้องสำหรับการตรวจสอบความถูกต้องของผู้ใช้และการตรวจสอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="62294-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62294-134">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="62294-134">Additional resources</span></span>

[<span data-ttu-id="62294-135">ตั้งค่าฟังก์ชันการล็อกออนแบบขยายสำหรับ MPOS และ POS ระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="62294-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="62294-136">สร้างโพรไฟล์ฟังก์ชันการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="62294-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="62294-137"> ตั้งค่าคอนฟิกผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="62294-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]