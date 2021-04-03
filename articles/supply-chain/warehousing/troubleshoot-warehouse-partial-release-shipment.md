---
title: แก้ไขปัญหาการนำออกใช้บางส่วนและการจัดส่งบางส่วน
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการนำออกใช้บางส่วนและการจัดส่งบางส่วนใน Microsoft Dynamics 365 Supply Chain Management
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
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263285"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="315c0-103">แก้ไขปัญหาการนำออกใช้บางส่วนและการจัดส่งบางส่วน</span><span class="sxs-lookup"><span data-stu-id="315c0-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="315c0-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการนำออกใช้บางส่วนและการจัดส่งบางส่วนใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="315c0-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="315c0-105">สถานะนำออกใช้ของใบสั่งขายยังคงถูกนำออกใช้บางส่วนแม้หลังจากออกใบแจ้งหนี้ใบสั่งขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="315c0-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="315c0-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="315c0-106">Issue description</span></span>

<span data-ttu-id="315c0-107">ใบสั่งขายเป็นใบสั่งการจัดส่ง แต่มีสินค้าหนึ่งรายการขึ้นไปที่มีวิธีการจัดส่งที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="315c0-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="315c0-108">หลังจากออกใบแจ้งหนี้ใบสั่งแล้ว ยังคงมีสถานะ *นำออกใช้แล้วบางส่วน*</span><span class="sxs-lookup"><span data-stu-id="315c0-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="315c0-109">ตัวอย่างเช่น ใบสั่งขายมีสองสินค้ารายการ ได้แก่ หนึ่งสำหรับการจัดส่ง และหนึ่งสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="315c0-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="315c0-110">ทั้งการจัดส่งและการเบิกสินค้าเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="315c0-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="315c0-111">ดังนั้น ทั้งสองรายการได้ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="315c0-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="315c0-112">อย่างไรก็ตาม สถานะนำออกใช้ยังคงแสดงเป็น *นำออกใช้แล้วบางส่วน* ซึ่งเป็นการทำให้เข้าใจผิด</span><span class="sxs-lookup"><span data-stu-id="315c0-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="315c0-113">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="315c0-113">Issue resolution</span></span>

<span data-ttu-id="315c0-114">สถานะนำออกใช้ใช้เฉพาะกับรายการใบสั่งที่มีการเปิดใช้งานสินค้าสำหรับการจัดการคลังสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="315c0-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="315c0-115">สถานะนำออกใช้ยังคงเป็น *นำออกใช้บางส่วน* ในสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="315c0-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="315c0-116">Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="315c0-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="315c0-117">อาจมีการเพิ่มส่วนขยายเป็นส่วนหนึ่งของกระบวนการบันทึกการจัดส่งและการออกใบแจ้งหนี้เพื่ออัพเดตสถานะการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="315c0-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]