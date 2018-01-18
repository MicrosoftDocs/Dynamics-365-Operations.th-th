---
title: "ส่งใบสั่งจากร้านค้าอื่น"
description: "หัวข้อนี้อธิบายถึงลักษณะการทำงานค่าธรรมเนียมการส่ง"
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 9f9681d1fa4bf2c1f11c9642f4b3629a8518d316
ms.contentlocale: th-th
ms.lasthandoff: 01/18/2018

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="5dea9-103">ส่งใบสั่งจากร้านค้าอื่น</span><span class="sxs-lookup"><span data-stu-id="5dea9-103">Ship an order from a different store</span></span>

<span data-ttu-id="5dea9-104">ด้วยคุณลักษณะค่าธรรมเนียมการส่งใน Dynamics 365 for Retail ใบสั่งของลูกค้าสามารถถูกสั่งในร้านค้าหนึ่ง และถูกจัดส่งจากร้านค้าอื่นได้</span><span class="sxs-lookup"><span data-stu-id="5dea9-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="5dea9-105">ใบสั่งของลูกค้าในการขายหน้าร้าน (POS) ไคลเอนต์สนับสนุนตัวเลือกการเติมสินค้าหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5dea9-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="5dea9-106">ตัวอย่างบางรายการของตัวเลือกการเติมสินค้าประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="5dea9-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="5dea9-107">เบิกสินค้าจากร้านค้าเดียวกันในวันที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="5dea9-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="5dea9-108">เบิกสินค้าจากร้านค้าที่แตกต่างกันในวันที่เดียวกันหรือวันที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="5dea9-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="5dea9-109">จัดส่งจากคลังสินค้าสำหรับจัดส่งเริ่มต้นซึ่งถูกมอบหมายให้กับร้านค้า และจัดส่งในวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="5dea9-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="5dea9-110">คุณลักษณะค่าธรรมเนียมการส่งใช้การดำเนินงาน POS ต่อไปนี้: จัดส่งผลิตภัณฑ์ทั้งหมด และจัดส่งผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5dea9-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="5dea9-111">ซึ่งช่วยให้เจ้าหน้าที่จัดเก็บสามารถเลือกสถานที่ "จัดส่งจาก" ที่ใบสั่งหรือรายการใบสั่งสามารถถูกเติมเต็มได้</span><span class="sxs-lookup"><span data-stu-id="5dea9-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="5dea9-112">โดยค่าเริ่มต้น ที่ตั้ง "จัดส่งจาก" เป็นคลังสินค้าสำหรับจัดส่งที่เชื่อมโยงกับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5dea9-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="5dea9-113">อย่างไรก็ตาม เจ้าหน้าที่จัดเก็บสามารถเปลี่ยนสถานที่เก็บนี้ และเลือกร้านค้าใดๆ ที่ถูกกำหนดไว้ในกลุ่มรหัสที่ตั้งร้านค้าที่ถูกกำหนดให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5dea9-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="5dea9-114">ความสามารถในการการเลือกที่อยู่ "จัดส่งไปยัง" ยังคงไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5dea9-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="5dea9-115">วิธีการจัดส่งที่สามารถใช้ในกาเติมเต็มรายการใบสั่ง เป็นไปตามการตั้งค่าคอนฟิกโหมดการจัดส่งสำหรับผลิตภัณฑ์และที่อยู่ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5dea9-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="5dea9-116">เนื่องจากมีการรักษากฎเกี่ยวกับโหมดการจัดส่งถูกในศูนย์ควบคุมการขายปลีก (HQ) เท่านั้น ไคลเอนต์ POS ทำให้การเรียกแบบเรียลไทม์จะนำโหมดการจัดส่งสำหรับรายการการจัดส่งที่ถูกต้องมาใช้</span><span class="sxs-lookup"><span data-stu-id="5dea9-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


