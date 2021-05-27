---
title: กำหนดค่าการรับรองความถูกต้อง Azure Active Directory สำหรับการลงชื่อเข้าใช้ POS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิก Azure Active Directory เป็นวิธีการรับรองความถูกต้องใน Microsoft Dynamics 365 Commerce ขายหน้าร้าน
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: e271bbae84605b4adace1809b53b7cbdb6932da0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020022"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="ef702-103">กำหนดค่าการรับรองความถูกต้อง Azure Active Directory สำหรับการลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="ef702-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ef702-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิก Azure Active Directory (Azure AD) เป็นวิธีการรับรองความถูกต้องใน Microsoft Dynamics 365 Commerce ขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="ef702-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="ef702-105">ผู้ค้าปลีกที่ใช้ Dynamics 365 Commerce พร้อมกับบริการอื่นๆ ของ Microsoft Cloud เช่น Microsoft Azure, Microsoft 365 และ Microsoft Teams โดยทั่วไปต้องการใช้ Azure AD ในการจัดการข้อมูลส่วนบุคคลของผู้ใช้จากส่วนกลางเพื่อประสบการณ์การลงชื่อเข้าใช้ที่ปลอดภัยและต่อเนื่องระหว่างแอพลิเคชันต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ef702-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="ef702-106">เมื่อต้องการใช้ Azure AD การรับรองความถูกต้องของ Commerce POS คุณต้องตั้งค่าคอนฟิก Azure AD เป็นวิธีการรับรองความถูกต้องในศูนย์ควบคุม Commerce ก่อน</span><span class="sxs-lookup"><span data-stu-id="ef702-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="ef702-107">ตั้งค่าคอนฟิกวิธีการรับรองความถูกต้อง POS</span><span class="sxs-lookup"><span data-stu-id="ef702-107">Configure POS authentication method</span></span>

<span data-ttu-id="ef702-108">หากต้องการตั้งค่าคอนฟิกวิธีการรับรองความถูกต้อง POS ในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ef702-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="ef702-109">ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> โพรไฟล์ POS \> โพรไฟล์ฟังก์ชัน** แล้วเลือกโพรไฟล์ที่จะเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ef702-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="ef702-110">ในส่วน **ล็อกออนของพนักงาน POS** ของแท็บด่วน **ฟังก์ชัน** ให้เลือกตัวเลือกวิธีการรับรองความถูกต้องที่ต้องการจากรายการแบบหล่นลงของ **วิธีการรับรองความถูกต้องของล็อกออน**</span><span class="sxs-lookup"><span data-stu-id="ef702-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="ef702-111">**วิธีการรับรองความถูกต้องในการล็อกออน** จะมีสามตัวเลือกดังนี้</span><span class="sxs-lookup"><span data-stu-id="ef702-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="ef702-112">**รหัสบุคลากรและรหัสผ่าน** - ตัวเลือกนี้เป็นค่าเริ่มต้นต้องการให้ผู้ใช้ POS ป้อนรหัสบุคลากรและรหัสผ่านเพื่อล็อกอินเข้าสู่ POS และเข้าถึงฟังก์ชันแทนที่ของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="ef702-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="ef702-113">**Azure AD โดยไม่มีการลงชื่อเข้าใช้ครั้งเดียว** - ตัวเลือกนี้ต้องการให้ผู้ใช้ POS ใช้ข้อมูลส่วนบุคคล Azure AD เพื่อล็อกอินเข้าสู่ POS และเข้าถึงฟังก์ชันแทนที่ของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="ef702-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="ef702-114">เมื่อรีเฟรชหรือเปิดไคลเอนต์ POS อีกครั้ง ผู้ใช้ POS ต้องระบุข้อมูลส่วนบุคคล Azure AD เพื่อล็อกอินอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ef702-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="ef702-115">**Azure AD ที่มีการลงชื่อเข้าใช้ครั้งเดียว** - เมื่อเลือกตัวเลือกนี้ ผู้ใช้ POS จะสามารถล็อกอินเข้าสู่ Cloud POS (CPOS) โดยใช้ข้อมูลส่วนบุคคล Azure AD ที่ใช้งานอยู่ ซึ่งใช้งานโดยเว็บแอพลิเคชันอื่นๆ ในเว็บเบราเซอร์เดียวกัน หรือล็อกอินเข้าสู่ Modern POS (MPOS) โดยใช้ข้อมูลส่วนบุคคล Azure AD ที่ล็อกอินเข้าสู่ Windows</span><span class="sxs-lookup"><span data-stu-id="ef702-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="ef702-116">ทั้งสองวิธีอนุญาตให้ลงชื่อเข้าใช้ได้โดยไม่ต้องป้อนข้อมูลส่วนบุคคล Azure AD บนหน้าจอการลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="ef702-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="ef702-117">อย่างไรก็ตาม การเข้าใช้งานฟังก์ชันแทนที่ของผู้จัดการ POS จะยังคงต้องใช้การลงชื่อเข้าใช้ โดยใช้ข้อมูลส่วนบุคคล Azure AD</span><span class="sxs-lookup"><span data-stu-id="ef702-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="ef702-118">ไปที่ **Retail และ Commerce > Retail และ Commerce IT > กําหนดการกระจาย** และรันงาน **1070 (การตั้งค่าคอนฟิกช่องทาง)** เพื่อซิงโครไนส์ การตั้งค่าโพรไฟล์ฟังก์ชันล่าสุดไปยังไคลเอนต์ POS</span><span class="sxs-lookup"><span data-stu-id="ef702-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="ef702-119">ตัวเลือกวิธีการรับรองความถูกต้อง **Azure AD แบบไม่มีการลงชื่อเข้าใช้ครั้งเดียว** จะแทนที่ตัวเลือก **Azure Active Directory** ใน Commerce เวอร์ชัน 10.0.18 และรุ่นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ef702-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="ef702-120">การรับรองความถูกต้อง Azure AD ต้องใช้การเชื่อมต่ออินเทอร์เน็ตที่ใช้งานอยู่ และจะใช้ไม่ได้เมื่อ POS ออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="ef702-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="ef702-121">เชื่อมโยงบัญชี Azure AD กับผู้ใช้ POS</span><span class="sxs-lookup"><span data-stu-id="ef702-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="ef702-122">เมื่อต้องการใช้ Azure AD เป็นวิธีการรับรองความถูกต้อง POS คุณต้องเชื่อมโยงบัญชี Azure AD กับผู้ใช้ POS ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="ef702-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="ef702-123">การเชื่อมโยงบัญชี Azure AD กับผู้ใช้ POS ในศูนย์ควบคุม Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ef702-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="ef702-124">ไปที่ **Retail และ Commerce > พนักงาน > ผู้ปฏิบัติงาน** และเปิดเรกคอร์ดผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="ef702-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="ef702-125">บนบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **Commerce** จากนั้น ภายใต้ **ข้อมูลเฉพาะตัวภายนอก** ให้เลือก **เชื่อมโยงข้อมูลเฉพาะตัวที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="ef702-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="ef702-126">ในกล่องโต้ตอบ **ใช้ข้อมูลเฉพาะตัวภายนอกที่มีอยู่** ให้เลือก **ค้นหาโดยใช้อีเมล** ป้อนที่อยู่อีเมล Azure AD แล้วเลือก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="ef702-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="ef702-127">เลือกบัญชี Azure AD ที่จะส่งคืน จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ef702-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="ef702-128">หลังจากตั้งค่าคอนฟิกขั้นตอนด้านบนแล้ว ฟิลด์ **นามแฝง** **UPN** และ **ตัวระบุย่อยภายนอก** บนแท็บ **Commerce** ของหน้ารายละเอียดของผู้ปฏิบัติงานจะถูกกรอกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ef702-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="ef702-129">คุณต้องรันงาน **1060 (พนักงาน)** ใน **Retail และ Commerce > Retail และ Commerce IT > กำหนดการการกระจาย** เพื่อซิงโครไนส์ข้อมูลผู้ใช้ POS และบัญชี Azure AD ล่าสุด ไปยังช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ef702-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="ef702-130">ตามแนวทางปฏิบัติ หลังจากที่ข้อมูลผู้ปฏิบัติงาน เช่น รหัสผ่าน สิทธิ์ POS บัญชี Azure AD ที่เชื่อมโยง หรือสมุดที่อยู่ของพนักงานมีการอัพเดตในศูนย์ควบคุม Commerce แล้ว ขอแนะนำว่าควรรันงาน **1060 (พนักงาน)** เพื่อซิงโครไนส์ข้อมูลผู้ปฏิบัติงานล่าสุดกับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ef702-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="ef702-131">จากนั้นไคลเอนต์ POS จะสามารถดึงข้อมูลที่ถูกต้องสำหรับการตรวจสอบความถูกต้องของผู้ใช้ และการตรวจสอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="ef702-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="ef702-132">ล็อคเครื่องบันทึกเงินสด POS และออกจากระบบ โดยใช้การรับรองความถูกต้อง Azure AD</span><span class="sxs-lookup"><span data-stu-id="ef702-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="ef702-133">สิ่งต่อไปนี้จะเกิดขึ้นเมื่อ POS ได้รับการตั้งค่าคอนฟิกให้ใช้วิธีการบรองความถูกต้อง Azure AD:</span><span class="sxs-lookup"><span data-stu-id="ef702-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="ef702-134">ฟังก์ชัน **ล็อคเครื่องบันทึกเงินสด** จะไม่พร้อมใช้งานในแอพลิเคชัน POS</span><span class="sxs-lookup"><span data-stu-id="ef702-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="ef702-135">ฟังก์ชัน **ล็อคโดยอัตโนมัติ** จะทำงานเช่นเดียวกับ **ฟังก์ชันล็อกออฟโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="ef702-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="ef702-136">หากผู้ใช้ POS เลือก **ล็อกออฟ** ผู้ใช้จะได้รับการขอให้ล็อกอินโดยใช้ข้อมูลประจำตัว Azure AD ในครั้งถัดไปที่ POS เปิดใช้ ไม่ว่าการลงชื่อเข้าใช้ครั้งเดียวจะเปิดใช้งานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ef702-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="ef702-137">ฟังก์ชันการแทนที่ของผู้จัดการพร้อมด้วยการรับรองความถูกต้อง Azure AD</span><span class="sxs-lookup"><span data-stu-id="ef702-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="ef702-138">เมื่อ POS ได้รับการตั้งค่าคอนฟิกให้ใช้การรับรองความถูกต้อง Azure AD ฟังก์ชันการแทนที่ของผู้จัดการจะเปิดกล่องโต้ตอบที่พร้อมต์ถามข้อมูลส่วนบุคคล Azure AD ของผู้ใช้ที่เป็นผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="ef702-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="ef702-139">หลังจากที่อนุมัติการลงชื่อเข้าใช้ของผู้จัดการ ข้อมูลประจำตัว Azure AD ของผู้จัดการจะถูกทิ้งและข้อมูลส่วนบุคคลของผู้ใช้ Azure AD ก่อนหน้านี้จะถูกใช้ เพื่อดําเนินการ POS ในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="ef702-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="ef702-140">ใน Commerce เวอร์ชัน 10.0.18 และก่อนหน้านั้น ฟังก์ชันแทนที่ของผู้จัดการไม่สนับสนุน Azure AD</span><span class="sxs-lookup"><span data-stu-id="ef702-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="ef702-141">ต้องระบุรหัสบุคลากรและรหัสผ่าน แม้ว่า POS จะมีการตั้งค่าคอนฟิกให้ใช้วิธีการรับรองความถูกต้อง Azure AD</span><span class="sxs-lookup"><span data-stu-id="ef702-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="ef702-142">เมื่อใช้ CPOS กับเว็บเบราเซอร์ Safari บนอุปกรณ์ Apple iOS คุณต้องปิด **การบล็อคป๊อปอัพ** ในการตั้งค่า Safari สำหรับฟังก์ชันแทนที่ของผู้จัดการ เพื่อใช้งานการรับรองความถูกต้อง Azure AD</span><span class="sxs-lookup"><span data-stu-id="ef702-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="ef702-143">แนวทางที่พึงปฏิบัติด้านความปลอดภัยสำหรับการรับรองความถูกต้อง Azure AD- ตาม POS บนอุปกรณ์ที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="ef702-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="ef702-144">ผู้ค้าปลีกหลายคนตั้งค่าสภาพแวดล้อมร้านค้าปลีกของพวกเขาในลักษณะที่ผู้ใช้หลายคนต้องเข้าถึงแอพลิเคชัน POS จากอุปกรณ์จริงที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="ef702-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="ef702-145">ในบริบทนั้น ขณะที่การลงชื่อเข้าใช้ครั้งเดียวจะให้ประสบการณ์การรับรองความถูกต้องที่สะดวกและไม่มีขอบเขต ก็อาจสร้างลูปความปลอดภัยโดยที่ผู้ใช้ POS ปัจจุบันอาจไม่รับรู้ได้ว่าข้อมูลส่วนบุคคลของผู้ใช้คนอื่น ถูฏใช้ในการดําเนินธุรกรรมหรือการดําเนินงานใน POS</span><span class="sxs-lookup"><span data-stu-id="ef702-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="ef702-146">ก่อนที่คุณจะตั้งค่าคอนฟิก POS เพื่อใช้วิธีการรับรองความถูกต้อง Azure AD เราแนะนำเป็นอย่างยิ่งให้ทบทวนนโยบายความปลอดภัยของคุณ และการตั้งค่าการลงชื่อเข้าใช้ของอุปกรณ์ที่ใช้ร่วมกัน เพื่อตัดสินว่าตัวเลือกใดที่เหมาะสมที่สุด</span><span class="sxs-lookup"><span data-stu-id="ef702-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="ef702-147">ถ้าสภาพแวดล้อมการขายปลีกของคุณใช้บัญชีที่ใช้ร่วมกัน (ตัวอย่างเช่น บัญชีเฉพาะที่) สำหรับการลงชื่อเข้าใช้อุปกรณ์จริง เราแนะนำให้ใช้ตัวเลือก **Azure AD แบบไม่มีการลงชื่อเข้าใช้ครั้งเดียว**</span><span class="sxs-lookup"><span data-stu-id="ef702-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="ef702-148">ซึ่งช่วยให้มั่นใจว่าผู้ใช้ POS แต่ละคนจะมีข้อมูลส่วนบุคคล Azure AD ที่จะล็อกอินเข้าสู่ POS อย่างชัดแจ้ง</span><span class="sxs-lookup"><span data-stu-id="ef702-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="ef702-149">ถ้าสภาพแวดล้อมการขายปลีกของคุณต้องการให้พนักงานใช้บัญชี Azure AD ของพวกเขาเองเพื่อล็อกอินเข้าสู่ POS และโฮสต์อุปกรณ์จริง เราแนะนำให้ใช้ตัวเลือก **Azure AD แบบการลงชื่อเข้าใช้ครั้งเดียว**</span><span class="sxs-lookup"><span data-stu-id="ef702-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef702-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ef702-150">Additional resources</span></span>

[<span data-ttu-id="ef702-151"> ตั้งค่าคอนฟิกผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="ef702-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="ef702-152">สร้างโพรไฟล์ฟังก์ชันการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="ef702-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="ef702-153">ตั้งค่าฟังก์ชันการล็อกออนแบบขยายสำหรับ MPOS และ POS ระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="ef702-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="ef702-154">แนวทางที่พึงปฏิบัติด้านความปลอดภัยของ Cloud POS ในสภาพแวดล้อมที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="ef702-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
