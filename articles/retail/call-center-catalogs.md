---
title: "แค็ตตาล็อกของศูนย์บริการ"
description: "บทความนี้อธิบายถึงศูนย์บริการ – ฟังก์ชันเฉพาะสำหรับแค็ตตาล็อกใน Microsoft Dynamics 365 for Retail"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e5a97ab749259fcc97b269b0134792820ebf13af
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="29254-103">แค็ตตาล็อกของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="29254-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="29254-104">บทความนี้อธิบายถึงศูนย์บริการ – ฟังก์ชันเฉพาะสำหรับแค็ตตาล็อกใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="29254-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="29254-105">ในศูนย์บริการทางโทรศัพท์ คุณสามารถใช้แค็ตตาล็อกผลิตภัณฑ์เพื่อระบุผลิตภัณฑ์ที่คุณต้องการเสนอให้แก่ลูกค้า </span><span class="sxs-lookup"><span data-stu-id="29254-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="29254-106">ศูนย์บริการโดยทั่วไปใช้แค็ตตาล็อกที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="29254-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="29254-107">การออกแบบและการผลิตของแค็ตตาล็อกที่พิมพ์จะถูกจัดการนอก Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="29254-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="29254-108">อย่างไรก็ตาม คุณสามารถสร้างและจัดเก็บแค็ตตาล็อกในรูปแบบดิจิทัลได้โดยการใช้เพจเดียวกันกับที่คุณใช้การตั้งค่าแค็ตตาล็อกการขายปลีกออนไลน์</span><span class="sxs-lookup"><span data-stu-id="29254-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="29254-109">ก่อนที่คุณสามารถสร้างแค็ตตาล็อกได้ คุณต้องตั้งค่าการจัดประเภทผลิตภัณฑ์และมอบการจัดประเภทให้กับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="29254-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="29254-110">จากนั้นคุณเพิ่มผลิตภัณฑ์ไปยังแค็ตตาล็อกได้โดยการเลือกผลิตภัณฑ์จากการจัดประเภทเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="29254-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="29254-111">หลังจากที่ได้เพิ่มผลิตภัณฑ์ลงในแค็ตตาล็อกจนแค็ตตาล็อกเสร็จสมบูรณ์แล้ว คุณต้องตรวจสอบความถูกต้องของแค็ตตาล็อกเพื่อตรวจสอบความถูกต้องของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="29254-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="29254-112">จากนั้นคุณต้องส่งแค็ตตาล็อกเพื่อตรวจทานและอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="29254-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="29254-113">หลังจากที่มีอนุมัติแค็ตตาล็อก จึงจะสามารถเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="29254-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="29254-114">เมื่อสร้างแค็ตตาล็อกศูนย์บริการแล้ว คุณสามารถทำสแนปช็อตของข้อมูลแค็ตตาล็อกได้เมื่อมีการเผยแพร่แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="29254-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="29254-115">ฟังก์ชันสแนปช็อตนี้ช่วยให้คุณเข้าถึงแค็ตตาล็อกรุ่นใดรุ่นหนึ่งได้แม้ว่าแค็ตตาล็อกนั้นจะมีการเปลี่ยนแปลงและอัพเดตในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="29254-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="29254-116">แค็ตตาล็อกของศูนย์บริการสามารถตั้งค่าเพื่อให้รวมคุณสมบัติเสริมเหล่านี้เข้าไปด้วยได้</span><span class="sxs-lookup"><span data-stu-id="29254-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="29254-117">**รหัสต้นทาง** – รหัสต้นทางถูกใช้ในการติดตามการตอบสนองของลูกค้าที่มีต่อการส่งเมล์แค็ตตาล็อกเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="29254-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="29254-118">**ผลิตภัณฑ์ฟรี**– ผลิตภัณฑ์สามารถรวมอยู่ในใบสั่งของลูกค้าได้โดยที่ไม่มีค่าธรรมเนียมเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="29254-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="29254-119">ผลิตภัณฑ์เหล่านี้จะถูกเพิ่มโดยอัตโนมัติไปยังใบสั่งเมื่อรหัสต้นทางสำหรับแค็ตตาล็อกถูกป้อนลงในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="29254-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="29254-120">**สคริปต์**– สคริปต์คือข้อความที่ผู้ปฏิบัติงานของศูนย์บริการอ่านให้ลูกค้าฟังเมื่อมีการสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="29254-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="29254-121">สคริปต์สามารถรวมคำทักทายหรือคำแนะนำเกี่ยวกับการซื้อได้</span><span class="sxs-lookup"><span data-stu-id="29254-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="29254-122">**โครงร่างหน้า**– โครงร่างหน้าเก็บตำแหน่งหน้าของผลิตภัณฑ์ในแค็ตตาล็อกที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="29254-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="29254-123">ข้อมูลนี้ใช้สำหรับรายงานการวิเคราะห์พื้นที่แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="29254-123">This information is used for the catalog area analysis report.</span></span>





