---
title: ระบบขอให้คุณบันทึกการตั้งค่าความครอบคลุมสินค้าถึงแม้ว่าคุณจะไม่ได้เปลี่ยนแปลงข้อมูลใดๆ
description: ระบบขอให้คุณบันทึกการตั้งค่าความครอบคลุมสินค้าถึงแม้ว่าคุณจะไม่ได้เปลี่ยนแปลงข้อมูลใดๆ
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049492"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="17e87-103">ระบบขอให้คุณบันทึกการตั้งค่าความครอบคลุมสินค้าถึงแม้ว่าคุณจะไม่ได้เปลี่ยนแปลงข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="17e87-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="17e87-104">หมายเลข KB: 4615588</span><span class="sxs-lookup"><span data-stu-id="17e87-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="17e87-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="17e87-105">Symptoms</span></span>

<span data-ttu-id="17e87-106">ในบางสถานการณ์ คุณอาจได้รับข้อความต่อไปนี้เมื่อคุณเปิดหน้า **ความครอบคลุมสินค้า** หลังจากที่คุณนําเข้าสินค้าผ่านเอนทิตี *ความครอบคลุมสินค้า V2*:</span><span class="sxs-lookup"><span data-stu-id="17e87-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="17e87-107">คุณต้องการบันทึกการเปลี่ยนแปลงของคุณก่อนที่จะปิดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="17e87-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="17e87-108">คุณจะได้รับข้อความนี้แม้ว่าคุณจะยังไม่ได้เปลี่ยนแปลงใดๆ</span><span class="sxs-lookup"><span data-stu-id="17e87-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="17e87-109">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="17e87-109">Resolution</span></span>

<span data-ttu-id="17e87-110">หน้า **ความครอบคลุมสินค้า** รวมตรรกะค่าเริ่มต้นที่ซับซ้อน ซึ่งอาจทําให้ข้อความแสดงขึ้นหลังจากที่มีการเปลี่ยนแปลงโดยตรงเมื่อเร็วๆ นี้ในฐานข้อมูล เช่น การนําเข้าเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="17e87-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="17e87-111">ตัวอย่างเช่น ฟิลด์เอนทิตี `AREGENERALSETTINGSOVERRIDDEN` มีการตั้งค่าเป็น *ไม่* แต่คุณนําเข้าไฟล์ที่มีค่าใหม่หรือที่ปรับเปลี่ยนแล้วของฟิลด์ เช่น `PRODUCTCOVERAGEGROUPID` และ/หรือ `VENDORACCOUNTNUMBER`</span><span class="sxs-lookup"><span data-stu-id="17e87-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="17e87-112">ในกรณีนี้ เนื่องจากฟิลด์ `AREGENERALSETTINGSOVERRIDDEN` มีการตั้งค่าเป็น *ไม่* ค่าของค่าจะถูกล้างข้อมูลโดยอัตโนมัติจากฟิลด์ เมื่อคุณเปิด **หน้าความครอบคลุมสินค้า** เป็นครั้งแรกหลังจากการนําเข้า</span><span class="sxs-lookup"><span data-stu-id="17e87-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="17e87-113">ถ้าคุณบันทึกการเปลี่ยนแปลงเป็นพร้อมต์ของกล่องข้อความ การเปลี่ยนแปลงเหล่านั้นจะถูกจัดเก็บไว้ในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="17e87-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="17e87-114">มิฉะนั้นคุณจะได้รับข้อความเดียวกันในครั้งถัดไปที่คุณเปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="17e87-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="17e87-115">เมื่อต้องการป้องกันลักษณะการนั่นแต่ยังรวมค่าส่ไว้่ฟิลด์เช่น การนํา `PRODUCTCOVERAGEGROUPID` เข้าเอนทิตี ให้ตั้งค่า `AREGENERALSETTINGSOVERRIDDEN` เป็น *ใช่* เมื่อคุณนําเข้า</span><span class="sxs-lookup"><span data-stu-id="17e87-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
