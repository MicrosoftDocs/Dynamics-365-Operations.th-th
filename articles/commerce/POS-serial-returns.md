---
title: ส่งคืนผลิตภัณฑ์ที่ควบคุมหมายเลขลำดับประจำสินค้าใน POS
description: หัวข้อนี้อธิบายความสามารถเกี่ยวกับการตรวจสอบความถูกต้องของสินค้าที่เป็นอนุกรม ซึ่งเป็นส่วนหนึ่งของกระบวนการส่งคืนในแอปพลิเคชันการขายหน้าร้าน Microsoft Dynamics 365 Commerce (POS)
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129833"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="e0df6-103">ส่งคืนผลิตภัณฑ์ที่ควบคุมหมายเลขลำดับประจำสินค้าใน POS</span><span class="sxs-lookup"><span data-stu-id="e0df6-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e0df6-104">หัวข้อนี้อธิบายความสามารถเกี่ยวกับการตรวจสอบความถูกต้องของสินค้าที่เป็นอนุกรม ซึ่งเป็นส่วนหนึ่งของกระบวนการส่งคืนในแอปพลิเคชันการขายหน้าร้าน Microsoft Dynamics 365 Commerce (POS)</span><span class="sxs-lookup"><span data-stu-id="e0df6-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="e0df6-105">ใน Commerce รุ่น 10.0.20 และใหม่กว่า จะมีคุณลักษณะใหม่ที่ชื่อ **ประสบการณ์การประมวลผลการส่งคืนแบบรวมใน POS** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e0df6-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="e0df6-106">เมื่อต้องการใช้การตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าระหว่างการประมวลผลใบสั่งส่งคืนสินค้าใน POS คุณต้องเปิดคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="e0df6-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="e0df6-107">หากต้องการข้อมูลเกี่ยวกับความสามารถอื่นๆ ที่มีคุณลักษณะนี้เมื่อเปิดคุณสมบัตินี้ โปรดดูที่ [สร้างการส่งคืนใน POS)](POS-returns.md)</span><span class="sxs-lookup"><span data-stu-id="e0df6-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="e0df6-108">หลังจากเปิดคุณลักษณะแล้ว ไม่สามารถปิดได้</span><span class="sxs-lookup"><span data-stu-id="e0df6-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="e0df6-109">ตัวเลือกการตรวจสอบความถูกต้องของการส่งคืนฑ์ที่กำหนดหมายเลขลำดับประจำสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="e0df6-109">Options for validating serialized returns</span></span>

<span data-ttu-id="e0df6-110">เมื่อเปิดคุณลักษณะ **ประสบการณ์การประมวลผลการส่งคืนแบบรวมใน POS** องค์กรสามารถตรวจสอบความถูกต้องของการส่งคืนสินค้าที่มีการควบคุมหมายเลขลำดับประจำสินค้าโดยผ่าน POS ได้</span><span class="sxs-lookup"><span data-stu-id="e0df6-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="e0df6-111">ความสามารถนี้สามารถแจ้งเตือนผู้ใช้ได้ ถ้าหมายเลขหมายเลขลำดับประจำสินค้าที่ส่งคืนแตกต่างจากหมายเลขหมายเลขลำดับประจำสินค้าที่ขาย</span><span class="sxs-lookup"><span data-stu-id="e0df6-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="e0df6-112">ใน Commerce รุ่น 10.0.20 และใหม่กว่า ข้อความที่ผู้ใช้ได้รับคือข้อความเตือนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e0df6-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="e0df6-113">ผู้ใช้สามารถประมวลผลการส่งคืนกับหมายเลขหมายเลขลำดับประจำสินค้าที่แตกต่างจากหมายเลขหมายเลขลำดับประจำสินค้าที่ขายครั้งแรกได้</span><span class="sxs-lookup"><span data-stu-id="e0df6-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="e0df6-114">เมื่อต้องการตั้งค่าคอนฟิกการตรวจสอบความถูกต้องของหมายเลขหมายเลขลำดับประจำสินค้าขององค์กรหลังจากคุณลักษณะ **ประสบการณ์การประมวลผลการส่งคืนแบบรวมใน POS** เปิดอยู่ ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ Commerce** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="e0df6-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="e0df6-115">บนแท็บ **สินค้าคงคลัง** บนแท็บด่วน **การดําเนินงานสินค้าคงคลังของร้านค้า** ให้ตั้งค่าตัวเลือก **เปิดใช้งาน การตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าบนการส่งคืน POS** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e0df6-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="e0df6-116">ประมวลผลการส่งคืนสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าแล้วใน POS</span><span class="sxs-lookup"><span data-stu-id="e0df6-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="e0df6-117">หากตัวเลือก **เปิดใช้การตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าบนการส่งคืน POS** ได้รับการตั้งค่าเป็น **ใช่** เมื่อมีการส่งคืนสินค้าที่ควบคุมหมายเลขลำดับประจำสินค้าผ่านทาง POS ผู้ใช้สามารถป้อนหมายเลขลำดับประจำสินค้า ให้กับรายการส่งคืนในบานหน้าต่างรายละเอียดในหน้า **ผลิตภัณฑ์ที่สามารถส่งคืนได้**</span><span class="sxs-lookup"><span data-stu-id="e0df6-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="e0df6-118">ถ้าหมายเลขลำดับประจำสินค้าที่ป้อนไม่ตรงกับหมายเลขลำดับประจำสินค้าเดิมที่ขายให้กับธุรกรรมการขาย ผู้ใช้จะได้รับข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="e0df6-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="e0df6-119">อย่างไรก็ตาม แอปพลิเคชันไม่ได้ป้องกันไม่ให้ผู้ใช้ลงรายการบัญชีการส่งคืนต่อไป</span><span class="sxs-lookup"><span data-stu-id="e0df6-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="e0df6-120">ปัจจุบัน POS สนับสนุนการตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้ารายการส่งคืนที่มีปริมาณที่สั่งไม่เกินหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="e0df6-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="e0df6-121">ถ้ารายการใบสั่งขายดั้งเดิมถูกสร้างขึ้นในช่องทางที่ไม่ใช่ POS และหากปริมาณที่สั่งไว้ของสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าแล้วในรายการขายที่ระบุว่ามีมากกว่าหนึ่งรายการ สินค้านั้นจะสามารถส่งคืนโดยผ่าน POS ได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0df6-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0df6-122">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e0df6-122">Additional resources</span></span>

[<span data-ttu-id="e0df6-123">สร้างการส่งคืนใน POS</span><span class="sxs-lookup"><span data-stu-id="e0df6-123">Create returns in POS</span></span>](POS-returns.md)
