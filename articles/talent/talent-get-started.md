---
title: "เริ่มต้นใช้งานกับ Microsoft Dynamics 365 for Talent"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการปรับใช้อินเทอร์เฟสผู้ใช้กับการกำหนดลักษณะของคุณ ตลอดจนเชื่อมต่อกับทรัพยากรวิธีใช้ที่พร้อมใช้งานภายในผลิตภัณฑ์ และบนไซต์ docs.microsoft.com"
author: rschloma
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: b2514b6ff7500863a312ee378be008a7dcfb7438
ms.contentlocale: th-th
ms.lasthandoff: 03/08/2018

---
# <a name="getting-started-with-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="7c534-103">การเริ่มต้นใช้งานกับ Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="7c534-103">Getting started with Microsoft Dynamics 365 for Talent</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="7c534-104">ใน Microsoft Dynamics 365 for Talent จะง่ายในการปรับเปลี่ยนอินเทอร์เฟสผู้ใช้ และการตั้งค่าตัวเลือกที่ทำให้ซอฟต์แวร์สะดวกสำหรับความต้องการของคุณมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c534-104">In Microsoft Dynamics 365 for Talent it's easy to modify the user interface and set options that make the software more intuitive for your needs.</span></span> <span data-ttu-id="7c534-105">หัวข้อนี้มีการเชื่อมโยงไปยังหัวข้อที่แสดงข้อมูลเกี่ยวกับวิธีการปรับใช้อินเทอร์เฟสผู้ใช้กับการกำหนดลักษณะของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c534-105">This topic includes links to topics that provide information on how to adapt the user interface to your preferences.</span></span> <span data-ttu-id="7c534-106">หัวข้อยังรวมถึงการเชื่อมโยงไปยังข้อมูล ที่สามารถช่วยคุณในการค้นหาข้อมูลในระบบได้อย่างมีประสิทธิภาพและอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7c534-106">The topic also includes links to information that can help you find information in the system efficiently and accurately.</span></span> 

> [!NOTE] 
> <span data-ttu-id="7c534-107">ผลิตภัณฑ์ต่อไปนี้มีความเกี่ยวข้องกันอย่างใกล้ชิด: Dynamics 365 for Finance and Operations, Enterprise edition; Dynamics 365 for Retail; และ Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="7c534-107">The following products are closely related: Dynamics 365 for Finance and Operations, Enterprise edition; Dynamics 365 for Retail; and Dynamics 365 for Talent.</span></span> <span data-ttu-id="7c534-108">ฟังก์ชันเดียวกันอาจปรากฏในผลิตภัณฑ์ทั้ง 3 ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7c534-108">The same functionality may appear in all 3 products.</span></span> <span data-ttu-id="7c534-109">ดังนั้น ในหัวข้อที่เกี่ยวข้องกับการขายปลีกเป็นหลัก ชื่อผลิตภัณฑ์จะเป็น Dynamics 365 for Retail ในหัวข้อที่เกี่ยวข้องกับ Talent หลัก ชื่อผลิตภัณฑ์จะเป็น Dynamics 365 for Talent และหัวข้อที่เกี่ยวข้องกับผลิตภัณฑ์หลัก ชื่อผลิตภัณฑ์จะเป็น Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7c534-109">As a result, in topics that are primarily related to Retail, the product name will be Dynamics 365 for Retail; in topics that are primarily related to Talent, the product name will be Dynamics 365 for Talent; and in topics that are related to the core product, the product name will be Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="7c534-110">หัวข้อที่เขียนขึ้นสำหรับหนึ่งผลิตภัณฑ์อาจนำไปใช้กับฟังก์ชันเดียวกันในผลิตภัณฑ์ที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="7c534-110">Topics that are written for one product may apply to the same functionality in a related product.</span></span>

### <a name="personalizing-talent"></a><span data-ttu-id="7c534-111">Talent ที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="7c534-111">Personalizing Talent</span></span> 
<span data-ttu-id="7c534-112">หัวข้อต่อไปนี้แสดงวิธีการตั้งค่าคุณลักษณะหลายอย่างใน Dynamics 365 for Talent ที่ทำให้ง่ายสำหรับคุณในการทำงานของคุณให้เสร็จสิ้นในเวลาที่เหมาะสมได้</span><span class="sxs-lookup"><span data-stu-id="7c534-112">The following topics show how to set up many features in Dynamics 365 for Talent that make it easier for you to get your work done in a timely manner.</span></span> 

-   <span data-ttu-id="7c534-113">[ปรับแต่งประสบการณ์ผู้ใช้](../fin-and-ops/get-started/personalize-user-experience.md) - หัวข้อนี้อธิบายวิธีการต่างๆ ที่คุณสามารถปรับแต่ง Talent และปรับใช้ส่วนต่างๆ ของผลิตภัณฑ์ให้เข้ากับการกำหนดลักษณะของคุณมากยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c534-113">[Personalize the user experience](../fin-and-ops/get-started/personalize-user-experience.md) - This topic explains the different ways in which you can personalize Talent and adapt parts of the product to more closely suite your preferences.</span></span>

-   <span data-ttu-id="7c534-114">[ตั้งค่าคอนฟิกและกรองข้อมูลพื้นที่ทำงาน](../fin-and-ops/get-started/configure-filter-workspaces.md) - หัวข้อนี้อธิบายวิธีการเปลี่ยนลักษณะปรากฏและลักษณะการทำงานของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="7c534-114">[Configure and filter workspaces](../fin-and-ops/get-started/configure-filter-workspaces.md) - This topic shows how you can change the appearance and behavior of workspaces.</span></span>

-   <span data-ttu-id="7c534-115">[แสดงหน้าแบบเคียงข้างกันโดยใช้ไอคอน เปิดในหน้าต่างใหม่](../fin-and-ops/get-started/display-pages-side-by-side.md) - ในบางกรณี จะมีประสิทธิภาพในการดูหน้าหลายหน้าแบบเคียงข้างกัน ซึ่งสามารถช่วยให้ง่ายขึ้นในการทำงานให้เสร็จสมบูรณ์ได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="7c534-115">[Display pages side-by-side using the Open in New Window icon](../fin-and-ops/get-started/display-pages-side-by-side.md) - In some cases, it's efficient to view multiple pages side-by-side, which can make it easier to complete tasks quickly.</span></span> <span data-ttu-id="7c534-116">หัวข้อนี้อธิบายวิธีการแสดงหน้าแบบเคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="7c534-116">This topic explains how to display pages side-by-side.</span></span> 

-   <span data-ttu-id="7c534-117">[แป้นพิมพ์ลัด](../fin-and-ops/get-started/shortcut-keys.md) - หัวข้อนี้แสดงรายการแป้นพิมพ์ลัดสำหรับโครงร่างแป้นพิมพ์ของสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="7c534-117">[Keyboard shortcuts](../fin-and-ops/get-started/shortcut-keys.md) - This topic lists keyboard shortcuts for the United States keyboard layout.</span></span> 

### <a name="accessing-information"></a><span data-ttu-id="7c534-118">การเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7c534-118">Accessing information</span></span>
<span data-ttu-id="7c534-119">หัวข้อต่อไปนี้อธิบายวิธีการใช้การค้นหา และคุณลักษณะการค้นหาและการกรอง เพื่อค้นหาข้อมูลได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="7c534-119">The following topics explain how to use lookups, and the search and filtering features, to find information quickly.</span></span> 

-   <span data-ttu-id="7c534-120">[ใช้การค้นหาเพื่อค้นหาข้อมูล](../fin-and-ops/get-started/use-lookups-to-find-information.md) - หัวข้อนี้อธิบายวิธีที่การค้นหาสามารถช่วยคุณค้นหาค่าที่ถูกต้องหรือที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="7c534-120">[Use lookups to find information](../fin-and-ops/get-started/use-lookups-to-find-information.md) - This topic shows how lookups can help you quickly find the correct or desired value.</span></span> <span data-ttu-id="7c534-121">หัวข้ออธิบายวิธีที่การค้นหาทำงาน และประกอบด้วยคำแนะนำเพื่อช่วยให้คุณสามารถเพิ่มประสิทธิภาพการใช้งานนั้นได้</span><span class="sxs-lookup"><span data-stu-id="7c534-121">The topic describes how lookups work and includes tips to help you optimize your use of them.</span></span>

-   <span data-ttu-id="7c534-122">[ตัวเลือกในการกรองข้อมูลและไวยากรณ์แบบสอบถาม](../fin-and-ops/get-started/advanced-filtering-query-options.md) - หัวข้อนี้อธิบายถึงการกรองข้อมูลและตัวเลือกการสอบถามที่พร้อมใช้งาน เมื่อคุณใช้ตัวดำเนินการ "ตรงกัน" ในกล่องโต้ตอบตัวกรอง/เรียงลำดับขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7c534-122">[Advanced filtering and query syntax](../fin-and-ops/get-started/advanced-filtering-query-options.md) - This topic describes the filtering and query options that are available when you use the "matches" operator in the Advanced filter/sort dialog box.</span></span>

-   <span data-ttu-id="7c534-123">[ค้นหาการนำทาง](../fin-and-ops/get-started/navigation-search.md) - หัวข้อนี้อธิบายวิธีการใช้ฟังก์ชันการค้นหาเพื่อนำทางไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="7c534-123">[Navigation search](../fin-and-ops/get-started/navigation-search.md) - This topic explains how to use the search functionality to navigate to pages.</span></span> <span data-ttu-id="7c534-124">แอพลิเคชัน Talent ประกอบด้วยจำนวนของพื้นที่และหน้า เพื่อช่วยคุณในการทำงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="7c534-124">The Talent application includes a number of areas and pages to help you perform various tasks.</span></span> <span data-ttu-id="7c534-125">การใช้คุณลักษณะค้นหาการนำทาง สามารถช่วยคุณค้นหาหน้าที่คุณต้องทำงานให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="7c534-125">Using the navigation search feature can help you quickly find the pages that you need to complete your tasks.</span></span> 

-   <span data-ttu-id="7c534-126">[การค้นหาการดำเนินการ](../fin-and-ops/get-started/action-search.md) - หัวข้อนี้อธิบายถึงฟังก์ชันการค้นหาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7c534-126">[Action search](../fin-and-ops/get-started/action-search.md) - This topic describes the action search functionality.</span></span> <span data-ttu-id="7c534-127">การดำเนินการค้นหาจะช่วยคุณค้นหาและดำเนินการที่เรียกใช้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="7c534-127">Action search will help you find and run actions on a page.</span></span> <span data-ttu-id="7c534-128">หน้าในผลิตภัณฑ์แสดงข้อมูลคำสั่งเป็นอันดับแรกในบานหน้าต่างการดำเนินการ ทั้งบานหน้าต่างการดำเนินการมาตรฐานที่ปรากฏขึ้นที่ด้านบนของหน้าและแถบเครื่องมือที่ปรากฏในส่วนต่างๆ ของหน้า</span><span class="sxs-lookup"><span data-stu-id="7c534-128">The pages in the product primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of a page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c534-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7c534-129">Additional resources</span></span>

### <a name="whats-new-and-in-development"></a><span data-ttu-id="7c534-130">มีอะไรใหม่และอะไรที่กำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="7c534-130">What's new and in development</span></span>
<span data-ttu-id="7c534-131">ไปที่ [แผนการทำงาน Microsoft Dynamics 365](https://roadmap.dynamics.com/#application=c6ae025f-e42a-e711-810d-3863bb363e80) เพื่อดูว่ามีการนำคุณลักษณะใหม่ใดออกใช้ และมีคุณลักษณะใหม่ใดบ้างที่กำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="7c534-131">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/#application=c6ae025f-e42a-e711-810d-3863bb363e80) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="7c534-132">บล็อก</span><span class="sxs-lookup"><span data-stu-id="7c534-132">Blogs</span></span>
<span data-ttu-id="7c534-133">คุณสามารถค้นหาความคิดเห็น ข่าวสาร และข้อมูลอื่นๆ เกี่ยวกับบัญชีเจ้าหนี้และการแก้ไขปัญหาอื่นๆ ได้ใน [Dynamics 365 for Talent](https://community.dynamics.com/enterprise/b/dynamics365fortalent)</span><span class="sxs-lookup"><span data-stu-id="7c534-133">You can find opinions, news, and other information about Accounts payable and other solutions on the [Dynamics 365 for Talent](https://community.dynamics.com/enterprise/b/dynamics365fortalent).</span></span> 

### <a name="videos"></a><span data-ttu-id="7c534-134">วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="7c534-134">Videos</span></span>
<span data-ttu-id="7c534-135">ดูวิดีโอวิธีการที่ตอนนี้มีอยู่บน [ช่อง YouTube ของ Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)</span><span class="sxs-lookup"><span data-stu-id="7c534-135">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>


