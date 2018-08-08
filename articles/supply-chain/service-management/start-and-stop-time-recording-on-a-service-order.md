---
title: "การเริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ"
description: "เริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ"
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 16d9f48ed38a5033fab94d45821f0ed6f7f1f011
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="start-and-stop-time-recording-on-a-service-order"></a><span data-ttu-id="39d32-103">การเริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="39d32-103">Start and stop time recording on a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="39d32-104">ใช้ขั้นตอนนี้เพื่อเริ่มต้น และหยุดการบันทึกเวลาสำหรับใบสั่งบริการที่มีกำหนดข้อตกลงระดับการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="39d32-104">Use this procedure to start and stop time recording for a service order for which a service level agreement is defined.</span></span>

## <a name="start-time-recording"></a><span data-ttu-id="39d32-105">เริ่มการจัดทำเรกคอร์ดเวลา</span><span class="sxs-lookup"><span data-stu-id="39d32-105">Start time recording</span></span>

1.  <span data-ttu-id="39d32-106">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="39d32-106">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="39d32-107">คลิกแท็บ **ใบสั่งบริการ** บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **ข้อตกลงระดับการบริการ** คลิก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="39d32-107">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Start**.</span></span>

3.  <span data-ttu-id="39d32-108">ป้อนวันที่และเวลาที่ควรเริ่มต้นการบันทึกเวลา</span><span class="sxs-lookup"><span data-stu-id="39d32-108">Enter the date and time that the time recording should be started.</span></span>

## <a name="stop-time-recording"></a><span data-ttu-id="39d32-109">หยุดการจัดทำเรกคอร์ดเวลา</span><span class="sxs-lookup"><span data-stu-id="39d32-109">Stop time recording</span></span>

1.  <span data-ttu-id="39d32-110">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="39d32-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="39d32-111">คลิกแท็บ **ใบสั่งบริการ** บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **ข้อตกลงระดับการบริการ** คลิก **หยุด**</span><span class="sxs-lookup"><span data-stu-id="39d32-111">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Stop**.</span></span>

3.  <span data-ttu-id="39d32-112">ป้อนวันที่และเวลาที่ควรหยุดการจัดทำเรกคอร์ดเวลา</span><span class="sxs-lookup"><span data-stu-id="39d32-112">Enter the date and time that the time recording should be stopped.</span></span>

4.  <span data-ttu-id="39d32-113">เลือก **เพิ่มเหตุผลการเพิกถอน** และเลือกรหัสเหตุผลในรายการ **รหัสเหตุผลของขั้นตอน** เพื่อระบุเหตุผลในการหยุดการบันทึกเวลา</span><span class="sxs-lookup"><span data-stu-id="39d32-113">Select **Add a revocation reason**, and select a reason code in the **Stage reason code** list to provide a reason for stopping the time recording.</span></span>


> [!NOTE]
> <P><span data-ttu-id="39d32-114">ถ้า <STRONG>รหัสเหตุผลที่เกินเวลา</STRONG> ถูกเลือกไว้ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการบริการ</STRONG> คุณต้องระบุรหัสเหตุผล ก่อนที่คุณจะสามารถหยุดการบันทึกเวลาได้</span><span class="sxs-lookup"><span data-stu-id="39d32-114">If <STRONG>Reason code on exceeding time</STRONG> is selected in the <STRONG>Service management parameters</STRONG> form, you must provide a reason code before you can stop the time recording.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="39d32-115">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="39d32-115">See also</span></span>

<span data-ttu-id="39d32-116">[การเริ่มต้นการจัดทำเรกคอร์ดเวลา SLA (แบบฟอร์ม)](https://technet.microsoft.com/en-us/library/hh242297\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="39d32-116">[Start SLA time recording (form)](https://technet.microsoft.com/en-us/library/hh242297\(v=ax.60\))</span></span>

<span data-ttu-id="39d32-117">[หยุดการจัดทำเรกคอร์ดเวลา SLA (แบบฟอร์ม)](https://technet.microsoft.com/en-us/library/hh242241\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="39d32-117">[Stop SLA time recording (form)](https://technet.microsoft.com/en-us/library/hh242241\(v=ax.60\))</span></span>

  



