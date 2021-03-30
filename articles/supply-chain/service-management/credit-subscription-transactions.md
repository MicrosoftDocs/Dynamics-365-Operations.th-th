---
title: เครดิตธุรกรรมการบอกรับเป็นสมาชิก
description: หัวข้อนี้แสดงวิธีการลงเครดิตธุรกรรมการบอกรับเป็นสมาชิก
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4238c625930767990d28a206b10a4d71841f2ad8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247513"
---
# <a name="credit-subscription-transactions"></a><span data-ttu-id="78b9a-103">เครดิตธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="78b9a-103">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="78b9a-104">เครดิตธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="78b9a-104">Credit subscription transactions</span></span>

1.  <span data-ttu-id="78b9a-105">คลิก **การจัดการงานบริการ** \> **ทั่วไป** \> **การบอกรับเป็นสมาชิกการบริการ** \> **การบอกรับเป็นสมาชิกการบริการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="78b9a-105">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="78b9a-106">เลือกการสั่งซื้อโดยบอกรับเป็นสมาชิกที่แนบไปกับธุรกรรมการสั่งซื้อโดยการบอกรับเป็นสมาชิกซึ่งคุณต้องการสร้างใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="78b9a-106">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="78b9a-107">เลือกแท็บ **วิเคราะห์** และจากนั้นคลิก **ธุรกรรมค่าธรรมเนียม** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="78b9a-107">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="78b9a-108">จากฟอร์ม **ธุรกรรมค่าธรรมเนียม** เลือกธุรกรรมซึ่งคุณต้องการสร้างใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="78b9a-108">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="78b9a-109">คลิก **ฟังก์ชัน** \> **เลือกสำหรับใบลดหนี้**</span><span class="sxs-lookup"><span data-stu-id="78b9a-109">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="78b9a-110">จากฟอร์ม **เลือกสำหรับใบลดหนี้** เลือกธุรกรรมที่คุณต้องการลงเครดิต และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="78b9a-110">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="78b9a-111">เมื่อคุณสร้างใบลดหนี้ ตรวจสอบให้แน่ใจว่าคุณเลือก <STRONG>ใบลดหนี้</STRONG></span><span class="sxs-lookup"><span data-stu-id="78b9a-111">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="78b9a-112">นี่จะถูกพบในรายการ <STRONG>วิธีการออกใบแจ้งหนี้</STRONG> ในกล่องโต้ตอบ <STRONG>สร้างใบแจ้งหนี้</STRONG></span><span class="sxs-lookup"><span data-stu-id="78b9a-112">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="78b9a-113">หากฟิลด์  **กลับรายการเครดิตการรับรู้** ในแบบฟอร์ม **พารามิเตอร์การจัดการงานบริการ** ได้รับการตั้งค่าเป็น **แบบกำหนดเอง** คุณต้องกลับธุรกรรมรายได้ค้างรับแต่ละรายการ ก่อนที่คุณจะสร้างข้อเสนอในใบลดหนี้สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="78b9a-113">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="78b9a-114">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="78b9a-114">See also</span></span>

[<span data-ttu-id="78b9a-115">การออกอินวอยซ์ธุรกรรมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="78b9a-115">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]