---
title: ค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย
description: หัวข้อนี้อธิบายวิธีสองวิธีในการจัดการค่าใช้จ่ายส่วนบุคคลของผู้ปฏิบัติงานใน Microsoft Dynamics 365 for Finance and Operations
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795018"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="2a339-103">ค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2a339-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a339-104">ระหว่างการเดินทางเพื่อไปทำธุรกิจของบริษัท บางครั้งพนักงานอาจชำระค่าใช้จ่ายส่วนตัวโดยใช้บัตรเครดิตของบริษัทของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="2a339-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="2a339-105">ถ้าคุณไม่กำหนดกระบวนการสำหรับการจัดการค่าใช้จ่ายส่วนบุคคล กระบวนการอนุมัติสำหรับรายงานค่าใช้จ่ายอาจจะหยุดชะงัก เมื่อพนักงานส่งรายงานค่าใช้จ่ายที่แสดงรายการของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="2a339-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="2a339-106">ใน Microsoft Dynamics 365 for Finance and Operations มีวิธีสองวิธีในการจัดการค่าใช้จ่ายส่วนบุคคลของผู้ปฏิบัติงาน:</span><span class="sxs-lookup"><span data-stu-id="2a339-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="2a339-107">**ชำระโดยพนักงาน** – องค์กรของคุณไม่ชำระค่าใช้จ่ายส่วนบุคคลที่ปรากฏในบิลสำหรับบัตรเครดิตของบริษัท</span><span class="sxs-lookup"><span data-stu-id="2a339-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="2a339-108">จะสร้างรายงานที่แสดงรายจ่ายส่วนตัวร่วมกับรายจ่ายของบริษัท ซึ่งถูกเรียกเก็บไปยังบัตรเครดิตของบริษัทแทน</span><span class="sxs-lookup"><span data-stu-id="2a339-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="2a339-109">**ชำระโดยบริษัท** – บริษัทของคุณชำระบิลทั้งหมดสำหรับบัตรเครดิตของบริษัท และจากนั้นหักบัญชีของพนักงานในส่วนที่เป็นรายจ่ายส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="2a339-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="2a339-110">คุณสามารถเลือกวิธีการที่องค์กรของคุณใช้ในหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย** ได้</span><span class="sxs-lookup"><span data-stu-id="2a339-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
