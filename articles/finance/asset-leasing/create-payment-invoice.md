---
title: สร้างใบแจ้งหนี้การชำระเงิน
description: หัวข้อนี้อธิบายวิธีการสร้างใบแจ้งหนี้ค่าเช่ารายเดือน คุณสามารถสร้างใบแจ้งหนี้สำหรับการเช่าแต่ละครั้ง หรือคุณสามารถใช้กระบวนการชุดงานเพื่อสร้างใบแจ้งหนี้สำหรับการเช่าหลายครั้งได้
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8d0b10993c61c64dadc00046907485f3886e2e01
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881191"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="c84f5-104">สร้างใบแจ้งหนี้การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c84f5-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c84f5-105">คุณสามารถสร้างใบแจ้งหนี้รายเดือนสำหรับการเช่าแต่ละครั้ง หรือคุณสามารถใช้กระบวนการชุดงานเพื่อสร้างใบแจ้งหนี้สำหรับการเช่าหลายครั้งได้</span><span class="sxs-lookup"><span data-stu-id="c84f5-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="c84f5-106">ขั้นตอนต่อไปนี้แสดงวิธีการสร้างการชำระค่าเช่าแต่ละรายการเมื่อมีการเปิดใช้งานพารามิเตอร์ **การชำระเงินให้แก่ผู้จัดจำหน่าย** บนหน้า **การตั้งค่าสมุดบัญชีการเช่า**</span><span class="sxs-lookup"><span data-stu-id="c84f5-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="c84f5-107">บนหน้า **สรุปการเช่า** เลือกการเช่าที่จะปรับปรุง แล้วเลือก **สมุดบัญชี \> กำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="c84f5-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="c84f5-108">เลือกการชำระเงินที่ต้องทำ แล้วเลือก **สร้างสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="c84f5-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="c84f5-109">คุณได้รับข้อความแจ้งว่ามีการสร้างสมุดรายวันสำหรับการชำระเงินที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c84f5-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="c84f5-110">เลือก **สมุดรายวันใบแจ้งหนี้** แล้วเลือกใบแจ้งหนี้ที่ต้องชำระ</span><span class="sxs-lookup"><span data-stu-id="c84f5-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="c84f5-111">บนแท็บ **บรรทัด** ให้ตรวจสอบรายการสมุดรายวันก่อนที่คุณจะลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="c84f5-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c84f5-112">โดยค่าเริ่มต้น บรรทัดใบแจ้งหนี้ของผู้จัดจำหน่ายที่สร้างขึ้นจะใช้โปรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายจากหน้า **พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="c84f5-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="c84f5-113">เลือกสมุดรายวันที่ถูกต้อง แล้วเลือกใบแจ้งหนี้ที่ต้องชำระ</span><span class="sxs-lookup"><span data-stu-id="c84f5-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="c84f5-114">สำหรับตัวอย่างนี้ พารามิเตอร์ **การชำระเงินให้แก่ผู้จัดจำหน่าย** เปิดใช้งานในสมุดบัญชีการเช่า</span><span class="sxs-lookup"><span data-stu-id="c84f5-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="c84f5-115">ใบแจ้งหนี้จะอยู่ในสมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c84f5-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="c84f5-116">ส่วน **ภาพรวม** แสดงสรุปของรายการสมุดรายวัน และส่วน **บรรทัด** จะแสดงรายละเอียดของบรรทัดสมุดรายวันที่แท้จริง</span><span class="sxs-lookup"><span data-stu-id="c84f5-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c84f5-117">ถ้ามีการปิดพารามิเตอร์ **การชำระเงินให้แก่ผู้จัดจำหน่าย** รายการสมุดรายวันการชำระเงินจะแสดงรายการอยู่บนหน้า **การเช่าสินทรัพย์** สำหรับสมุดบัญชีการเช่าและระบบจะสร้างรายการเงินประกันสินทรัพย์แทนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c84f5-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="c84f5-118">จะมีการลงรายการบัญชีการชำระค่าเช่าในชื่อสมุดรายวันที่ระบุไว้ในฟิลด์ **สมุดรายวันการเช่ารายเดือน**</span><span class="sxs-lookup"><span data-stu-id="c84f5-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="c84f5-119">หลังจากที่มีการลงรายการบัญชีธุรกรรมแล้ว คุณสามารถดูข้อมูลธุรกรรมและมูลค่าตามบัญชีของหนี้สินสัญญาเช่าโดยการเลือก **ธุรกรรมหนี้สิน** ในสมุดบัญชีการเช่า</span><span class="sxs-lookup"><span data-stu-id="c84f5-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="c84f5-120">ในกำหนดการชำระเงิน กล่องกาเครื่องหมาย **ลงรายการบัญชีสมุดรายวัน** จะถูกเลือก และบรรทัดจะแสดงหมายเลขสมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c84f5-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="c84f5-121">หลังจากที่มีการสร้างสมุดรายวันการชำระเงินและรายการสำหรับสมุดรายวันนั้นแล้ว คุณต้องย้อนกลับรายการก่อนจึงจะสามารถสร้างใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="c84f5-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
