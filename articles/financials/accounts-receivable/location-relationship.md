---
title: เพิ่มสถานที่และชนิดความสัมพันธ์ของฝ่าย
description: หัวข้อนี้อธิบายวิธีการเพิ่มสถานที่ใหม่และชนิดความสัมพันธ์ของฝ่าย
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 543784e8072f88c10f63e1b44921b9f2d37308c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "357507"
---
# <a name="add-location-roles-and-party-relationship-types"></a><span data-ttu-id="63982-103">เพิ่มบทบาทสถานที่และชนิดความสัมพันธ์ของฝ่าย</span><span class="sxs-lookup"><span data-stu-id="63982-103">Add location roles and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="63982-104">เพิ่มบทบาทสถานที่</span><span class="sxs-lookup"><span data-stu-id="63982-104">Add location roles</span></span>

<span data-ttu-id="63982-105">มีวิธีสองวิธีที่จะเพิ่มบทบาทสถานที่ใหม่สำหรับที่อยู่และข้อมูลผู้ติดต่อ:</span><span class="sxs-lookup"><span data-stu-id="63982-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="63982-106">เพิ่มผ่านทางหน้า **วัตถุประสงค์ของที่อยู่และข้อมูลการติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="63982-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="63982-107">บทบาทใหม่จะถูกบันทึกไปยังตาราง **LogisticsLocationRole** ที่มีชนิด = 0 ซึ่งบ่งชี้ว่า บทบาทไม่ใช่บทบาทของระบบที่กำหนดไว้ใน enum **LogisticsLocationRoleType** และส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="63982-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="63982-108">ผู้ใช้จะสามารถใช้บทบาทนี้ได้ เมื่อสร้างข้อมูลที่อยู่หรือผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="63982-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![วัตถุประสงค์ของที่อยู่และข้อมูลผู้ติดต่อ](media/Address-Contact.PNG)

-  <span data-ttu-id="63982-110">เพิ่มเข้าไปยังส่วนขยาย enum **LogisticsLocationRoleType** และปล่อยให้โปรแกรมเติมข้อมูลผ่านกระบวนการซิงค์ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63982-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="63982-111">สร้างการขยายไปยัง enum **LogisticsLocationRoleType** และเพิ่มบทบาทใหม่ในส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="63982-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="63982-113">สร้างไฟล์ทรัพยากรใหม่สำหรับบทบาทใหม่ และจากนั้น กำหนดค่าสำหรับคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="63982-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![ไฟล์ทรัพยากรใหม่](media/Resource.PNG)
        
    3.  <span data-ttu-id="63982-115">สร้างคลาสการเติมข้อมูล และให้วิธีการจัดการเพื่อเติมข้อมูลบทบาทใหม่</span><span class="sxs-lookup"><span data-stu-id="63982-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![การเติมข้อมูล](media/Dirdata.PNG)

    4.  <span data-ttu-id="63982-117">เพื่อทดสอบการนำเข้าข้อมูลบทบาทสถานที่ใหม่ คุณสามารถสร้างคลาสที่สามารถรันได้ และเรียกใช้ DirDataPopulation::insertLogisticsLocationRoles() ใน Main()</span><span class="sxs-lookup"><span data-stu-id="63982-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="63982-118">หลังจากกระบวนการนี้เสร็จสมบูรณ์ คุณควรเห็นบทบาทใหม่ที่เติมข้อมูลในตาราง **LogisticsLocationRole** ที่มีชนิด \> 0</span><span class="sxs-lookup"><span data-stu-id="63982-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="63982-119">บทบาทใหม่จะแสดงบนหน้า **วัตถุประสงค์ของที่อยู่และข้อมูลผู้ติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="63982-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![แทรกสถานที่ใหม่](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="63982-121">เพิ่มชนิดความสัมพันธ์ของฝ่าย</span><span class="sxs-lookup"><span data-stu-id="63982-121">Add party relationship types</span></span> 

<span data-ttu-id="63982-122">มีวิธีสองวิธีในการเพิ่มชนิดความสัมพันธ์ใหม่:</span><span class="sxs-lookup"><span data-stu-id="63982-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="63982-123">เพิ่มผ่านหน้า **ชนิดของความสัมพันธ์**</span><span class="sxs-lookup"><span data-stu-id="63982-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="63982-124">ความสัมพันธ์ใหม่จะถูกบันทึกลงใน **DirRelationshipTypeTable** ที่มี systemtype = 0</span><span class="sxs-lookup"><span data-stu-id="63982-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![ชนิดของความสัมพันธ์](media/Relationship.PNG)

-  <span data-ttu-id="63982-126">เพิ่มเข้าไปยังส่วนขยายของ enum **DirSystemRelationshipType** และปล่อยให้โปรแกรมเติมข้อมูลผ่านกระบวนการซิงค์ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63982-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="63982-127">สร้างการขยายไปยัง enum **DirSystemRelationshipType** และเพิ่มชนิดความสัมพันธ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="63982-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="63982-128">สร้างตัวเริ่มต้นสำหรับชนิดใหม่นี้</span><span class="sxs-lookup"><span data-stu-id="63982-128">Create an initializer for this new type.</span></span> <span data-ttu-id="63982-129">คุณสามารถค้นหาตัวอย่างที่หลากหลายในรหัสหลัก หนึ่งในนั้นคือ  **DirRelationshipTypeChildInitialize**</span><span class="sxs-lookup"><span data-stu-id="63982-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="63982-130">นี่คือคลาสตัวเริ่มต้นสำหรับชนิดความสัมพันธ์ของฝ่าย "รอง"</span><span class="sxs-lookup"><span data-stu-id="63982-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="63982-131">คุณสามารถเริ่มต้นด้วยตัวเริ่มต้นของคุณโดยการคัดลอกและการวางรหัสนี้ และจากนั้น อัพเดตพื้นที่ที่เน้น</span><span class="sxs-lookup"><span data-stu-id="63982-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="63982-133">เพื่อทดสอบการนำเข้าข้อมูลชนิดความสัมพันธ์ใหม่ คุณสามารถสร้างคลาสที่สามารถรันได้ และเรียกใช้ DirDataPopulation::insertDirRelationshipTypes() ใน Main()</span><span class="sxs-lookup"><span data-stu-id="63982-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="63982-134">คุณควรเห็นชนิดความสัมพันธ์ใหม่ใน **DirRelationshipTypeTable** และชนิดความสัมพันธ์ใหม่จะพร้อมใช้งานบนหน้า **ชนิดของความสัมพันธ์**</span><span class="sxs-lookup"><span data-stu-id="63982-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![คลาสที่สามารถรันได้](media/Runnable.PNG)
