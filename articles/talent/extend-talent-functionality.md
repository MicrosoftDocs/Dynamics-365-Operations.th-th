---
title: "ขยายฟังก์ชันของ Microsoft Dynamics 365 for Talent"
description: "ถ้าคุณได้สร้าง Microsoft PowerApps ใดๆ คุณสามารถเริ่มต้นแอพลิเคชันเหล่านั้นได้จากลิงค์ภายใน Microsoft Dynamics 365 for Talent"
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fbd5335f64865dfe6122d88b3bc45ec614fc0677
ms.openlocfilehash: c01a8f0106ee1181e973da50d428b8fc5e6e5a06
ms.contentlocale: th-th
ms.lasthandoff: 04/19/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="7502c-103">ขยายฟังก์ชันของ Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="7502c-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="7502c-104">ถ้าคุณได้สร้าง Microsoft PowerApps ใดๆ คุณสามารถเริ่มต้นแอพลิเคชันเหล่านั้นได้จากลิงค์ภายใน Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="7502c-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="7502c-105">เพื่อตั้งค่าการเข้าถึงแอพลิเคชันของคุณ คุณจะต้องตั้งค่าข้อมูลบางอย่างใน Talent บนหน้าการตั้งค่าคอนฟิกที่คุณสามารถเปิดได้จากพื้นที่ทำงาน **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="7502c-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="7502c-106">การตั้งค่าคอนฟิก PowerApps ที่ฝังอยู่ภายใน Talent</span><span class="sxs-lookup"><span data-stu-id="7502c-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="7502c-107">ใช้หน้า **ตั้งค่า Microsoft PowerApps ที่ฝังอยู่** เพื่อตั้งค่าคอนฟิกหน้า Talent ให้เริ่มต้นแอพลิเคชัน PowerApps</span><span class="sxs-lookup"><span data-stu-id="7502c-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="7502c-108">เพื่อเปิดหน้า **ตั้งค่า Microsoft PowerApps ที่ฝังอยู่** เปิดพื้นที่ทำงาน **การจัดการระบบ** และจากนั้นเปิดแท็บ **ลิงค์** เลือก **Microsoft PowerApps** จากกลุ่ม **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="7502c-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="7502c-109">มีการป้อนหรือตั้งค่าข้อมูลต่อไปนี้บนหน้านี้:</span><span class="sxs-lookup"><span data-stu-id="7502c-109">The following information is entered or set on this page:</span></span> 

 -  <span data-ttu-id="7502c-110">ชื่อที่เป็นคำอธิบายหรือตัวระบุสำหรับแอพลิเคชัน PowerApps แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="7502c-110">A descriptive name or identifier for each PowerApps application.</span></span>
 -  <span data-ttu-id="7502c-111">ตัวระบุเฉพาะ (GUID) สำหรับแต่ละแอพลิเคชันที่คุณเพิ่มไปยังเพจ Talent</span><span class="sxs-lookup"><span data-stu-id="7502c-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="7502c-112">รหัสแอปจะพร้อมใช้งานบนไซต์ PowerApps [powerapps.com](http://powerapps.com/)</span><span class="sxs-lookup"><span data-stu-id="7502c-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
 -  <span data-ttu-id="7502c-113">หน้าที่ผู้ใช้สามารถเปิดแอปหรือรายงาน</span><span class="sxs-lookup"><span data-stu-id="7502c-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="7502c-114">ไม่ใช่เพจ Talent ทั้งหมดที่สนับสนุนรายงาน PowerApps แบบฝัง และ Power BI</span><span class="sxs-lookup"><span data-stu-id="7502c-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="7502c-115">ป้อนชื่อภายในของหน้า ไม่ใช่ชื่อที่แสดงที่ปรากฏที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="7502c-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="7502c-116">เพื่อค้นหาชื่อภายใน เปิดเพจที่คุณต้องการชื่อภายใน และคลิกขวาที่ใดก็ได้บนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="7502c-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="7502c-117">เมื่อเปิดเมนู วางเมาส์ไว้เหนือรายการ **ข้อมูลฟอร์ม**</span><span class="sxs-lookup"><span data-stu-id="7502c-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="7502c-118">ชื่อแบบฟอร์มภายในจะแสดงขึ้นถัดจากรายการ **ข้อมูลฟอร์ม** ในเมนู</span><span class="sxs-lookup"><span data-stu-id="7502c-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
-   <span data-ttu-id="7502c-119">ระบุตัวควบคุมแบบฟอร์มที่แอพลิเคชันสามารถดึงข้อมูลบริบทได้</span><span class="sxs-lookup"><span data-stu-id="7502c-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="7502c-120">ตัวอย่างเช่น แอพลิเคชันอาจใช้ข้อมูลเกี่ยวกับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="7502c-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="7502c-121">ถ้าคุณป้อนหน้า **ผู้ปฏิบัติงาน** ในฟิลด์ **บริบท** หน้า **ผู้ปฏิบัติงาน** จะเปิดขึ้น เมื่อคุณเริ่มต้นแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="7502c-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="7502c-122">รายการใน **ฟิลด์บริบท** ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="7502c-122">An entry in the **Context field** is optional.</span></span> 
-   <span data-ttu-id="7502c-123">ตั้งค่าขนาดของกล่องโต้ตอบที่จะเรียกใช้แอพลิเคชัน PowerApps</span><span class="sxs-lookup"><span data-stu-id="7502c-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="7502c-124">กล่องโต้ตอบถูกกำหนดเป็น "เล็ก" หรือ "ใหญ่" เพื่อเพิ่มประสิทธิภาพอินเทอร์เฟสผู้ใช้ เมื่อแอพลิเคชันของคุณสำหรับการทำงานบนโทรศัพท์หรืออุปกรณ์ใหญ่ ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="7502c-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 


<span data-ttu-id="7502c-125">คุณยังสามารถระบุว่าแอพลิเคชันจะพร้อมใช้งานสำหรับนิติบุคคลใด หรือคุณสามารถทำให้พร้อมใช้งานสำหรับนิติบุคคลทั้งหมดของคุณได้</span><span class="sxs-lookup"><span data-stu-id="7502c-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="7502c-126">โดยค่าเริ่มต้น แอพลิเคชัน PowerApps ของคุณ จะพร้อมใช้งานกับนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7502c-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="7502c-127">การเปิดแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="7502c-127">Opening an application</span></span>
<span data-ttu-id="7502c-128">เมื่อคุณได้ตั้งค่าคอนฟิกแอพลิเคชัน PowerApps แบบฝัง ลิงค์ไปยังแอพลิเคชันที่คุณระบุ จะถูกเพิ่มลงในหน้าภายใน Talent</span><span class="sxs-lookup"><span data-stu-id="7502c-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="7502c-129">คลิกลิงค์เพื่อเปิดแอป</span><span class="sxs-lookup"><span data-stu-id="7502c-129">Click a link to open an application.</span></span> 



