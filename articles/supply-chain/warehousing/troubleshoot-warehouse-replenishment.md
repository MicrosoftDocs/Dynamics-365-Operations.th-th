---
title: การแก้ไขปัญหาการเติมสินค้าในคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการเติมสินค้าในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828093"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="15617-103">การแก้ไขปัญหาการเติมสินค้าในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="15617-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15617-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการเติมสินค้าในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="15617-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="15617-105">ฉันการเติมสินค้าได้รับข้อความข้อผิดพลาดต่อไปนี้: "งาน %1 ไม่สามารถปลดบล็อคได้ เนื่องจากมีงานการเติมสินค้าที่ยังไม่เสร็จสิ้น"</span><span class="sxs-lookup"><span data-stu-id="15617-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="15617-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="15617-106">Issue description</span></span>

<span data-ttu-id="15617-107">งานการเบิกสินค้าถูกบล็อคเนื่องจากงานการเติมสินค้าที่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="15617-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="15617-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="15617-108">Issue resolution</span></span>

<span data-ttu-id="15617-109">เมื่อคุณใช้การเติมสินค้าตามความต้องการของเวฟ ถ้าต้องเติมสถานที่เบิกสินค้าเพื่อตอบสนองความต้องการของใบสั่งต้นทาง ระบบจะสร้างทั้งงานการเติมสินค้าและงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="15617-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="15617-110">อย่างไรก็ตาม จะบล็อคงานการเบิกสินค้าจนกว่างานการเติมสินค้าจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="15617-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="15617-111">ลักษณะการทำงานนี้มีเจตนา เนื่องจากสถานที่เบิกสินค้าจะไม่มีสินค้าคงคลังเพียงพอยกเว้นว่างานการเติมสินค้าเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="15617-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="15617-112">ทำงานการเติมสินค้าให้เสร็จสมบูรณ์ แล้วประมวลผลงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="15617-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]