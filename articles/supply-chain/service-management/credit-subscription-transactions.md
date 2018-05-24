---
title: "การเครดิตธุรกรรมการบอกรับเป็นสมาชิก"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 14bc2c8667cf095006ea35d5ec8678d1a7cf4ea5
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="credit-subscription-transactions"></a><span data-ttu-id="3db3d-102">การเครดิตธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="3db3d-102">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="3db3d-103">การเครดิตธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="3db3d-103">Credit subscription transactions</span></span>

1.  <span data-ttu-id="3db3d-104">คลิก **การจัดการงานบริการ** \> **ทั่วไป** \> **การบอกรับเป็นสมาชิกการบริการ** \> **การบอกรับเป็นสมาชิกการบริการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="3db3d-104">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="3db3d-105">เลือกการสั่งซื้อโดยบอกรับเป็นสมาชิกที่แนบไปกับธุรกรรมการสั่งซื้อโดยการบอกรับเป็นสมาชิกซึ่งคุณต้องการสร้างใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="3db3d-105">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="3db3d-106">เลือกแท็บ **วิเคราะห์** และจากนั้นคลิก **ธุรกรรมค่าธรรมเนียม** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="3db3d-106">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="3db3d-107">จากฟอร์ม **ธุรกรรมค่าธรรมเนียม** เลือกธุรกรรมซึ่งคุณต้องการสร้างใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="3db3d-107">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="3db3d-108">คลิก **ฟังก์ชัน** \> **เลือกสำหรับใบลดหนี้**</span><span class="sxs-lookup"><span data-stu-id="3db3d-108">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="3db3d-109">จากฟอร์ม **เลือกสำหรับใบลดหนี้** เลือกธุรกรรมที่คุณต้องการลงเครดิต และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3db3d-109">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3db3d-110">เมื่อคุณสร้างใบลดหนี้ ตรวจสอบให้แน่ใจว่าคุณเลือก <STRONG>ใบลดหนี้</STRONG></span><span class="sxs-lookup"><span data-stu-id="3db3d-110">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="3db3d-111">นี่จะถูกพบในรายการ <STRONG>วิธีการออกใบแจ้งหนี้</STRONG> ในกล่องโต้ตอบ <STRONG>สร้างใบแจ้งหนี้</STRONG></span><span class="sxs-lookup"><span data-stu-id="3db3d-111">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="3db3d-112">หากฟิลด์  **กลับรายการเครดิตการรับรู้** ในแบบฟอร์ม **พารามิเตอร์การจัดการงานบริการ** ได้รับการตั้งค่าเป็น **แบบกำหนดเอง** คุณต้องกลับธุรกรรมรายได้ค้างรับแต่ละรายการ ก่อนที่คุณจะสร้างข้อเสนอในใบลดหนี้สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3db3d-112">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="3db3d-113">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3db3d-113">See also</span></span>

[<span data-ttu-id="3db3d-114">การออกอินวอยซ์ธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="3db3d-114">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 

