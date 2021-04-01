---
title: แก้ไขปัญหางานคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b1814f7b23efda2cabdb7bfc7bea4de6e3d6ec2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237070"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="4319d-103">แก้ไขปัญหางานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4319d-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4319d-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4319d-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="4319d-105">ฉันไม่สามารถย้ายป้ายทะเบียนที่มีสินค้าหมายเลขลำดับประจำสินค้าเมื่อการตัดสินค้าที่ว่างเปล่าได้และการรับสินค้าที่ว่างเปล่าสามารถทำได้บนกลุ่มมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="4319d-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4319d-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="4319d-106">Issue description</span></span>

<span data-ttu-id="4319d-107">คุณไม่สามารถย้ายป้ายทะเบียนได้โดยใช้รายการเมนู **การเคลื่อนย้าย** ถ้าหมายเลขลำดับประจำสินค้ามีการตั้งค่า *การตัดสินค้าที่ว่างเปล่าได้* และ *การรับสินค้าที่ว่างเปล่าได้* บนกลุ่มมิติการติดตาม และถ้ามีป้ายทะเบียนหลายใบในสถานที่เดียวกัน บางรายมีหมายเลขลำดับประจำสินค้าและบางอย่างที่ไม่มีหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="4319d-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4319d-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="4319d-108">Issue resolution</span></span>

<span data-ttu-id="4319d-109">ปัญหานี้จะได้รับการแก้ไขโดยการเปลี่ยนแปลงที่มีการปรับใช้ใน [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687)</span><span class="sxs-lookup"><span data-stu-id="4319d-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="4319d-110">การเปลี่ยนแปลงดังกล่าวจะทำให้ฟิลด์ **หมายเลขประจำสินค้า** ไม่จำเป็นต้องระบุเมื่อการตัดสินค้าที่ว่างเปล่าได้และการรับสินค้าที่ว่างเปล่าสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="4319d-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="4319d-111">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ในแอปคลังสินค้าเมื่อฉันประมวลผลการย้ายสินค้า: "เจ้าของสินค้าคงคลัง %1 ไม่ได้รับอนุญาตในกระบวนการนี้"</span><span class="sxs-lookup"><span data-stu-id="4319d-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4319d-112">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="4319d-112">Issue description</span></span>

<span data-ttu-id="4319d-113">มิติการติดตาม **เจ้าของ** หายไปเมื่อแอปคลังสินค้าใช้เพื่อทำการเคลื่อนย้าย</span><span class="sxs-lookup"><span data-stu-id="4319d-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="4319d-114">สมุดรายวันการโอนย้ายสินค้าคงคลังปกติจากไคลเอนต์ Supply Chain Management จะปรากฏขึ้นเพื่อให้คุณสามารถลงรายการบัญชีได้อย่างถูกต้อง และสามารถลงรายการบัญชีได้เฉพาะเมื่อมีการกรอกข้อมูลมิติ **เจ้าของ** ไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4319d-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4319d-115">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="4319d-115">Issue resolution</span></span>

<span data-ttu-id="4319d-116">Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4319d-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="4319d-117">ขณะนี้ กระบวนการจัดการคลังสินค้าสนับสนุนเฉพาะสินค้าคงคลังที่เป็นของนิติบุคคลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4319d-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]