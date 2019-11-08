---
title: สินทรัพย์ที่ยืม
description: หัวข้อนี้จะอธิบายวิธีการลงทะเบียนสินทรัพย์ที่ให้ยืมในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a365fb5b1e0126b9de56bcc84a14f2352208d4f
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571725"
---
# <a name="asset-loans"></a><span data-ttu-id="a23c1-103">สินทรัพย์ที่ยืม</span><span class="sxs-lookup"><span data-stu-id="a23c1-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a23c1-104">หากบริษัทของคุณได้รับสินทรัพย์สำหรับการซ่อมแซมหรืองานการบำรุงรักษาจากสถานที่ภายในหรือลูกค้า อย่างใดอย่างหนึ่ง และหากคุณกู้ยืมสินทรัพย์จากสถานที่หรือลูกค้าเหล่านั้น การจัดการสินทรัพย์สามารถติดตามสินทรัพย์ที่ยืมได้</span><span class="sxs-lookup"><span data-stu-id="a23c1-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="a23c1-105">ลงทะเบียนสินทรัพย์ที่ยืมในคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="a23c1-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="a23c1-106">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **คำขอการบำรุงรักษา** \> **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="a23c1-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a23c1-107">เลือกคำขอการบำรุงรักษาเพื่อลงทะเบียนสินทรัพย์ที่ยืม และจากนั้นเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a23c1-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="a23c1-108">ในหน้า **คำขอ** ให้เลือก **ส่งสินทรัพย์ที่ให้ยืม**</span><span class="sxs-lookup"><span data-stu-id="a23c1-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="a23c1-109">เลือกสินทรัพย์ และป้อนวันที่ส่งคืนที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="a23c1-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="a23c1-110">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a23c1-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="a23c1-111">คุณสามารถส่งสินทรัพย์ที่ให้ยืมได้เฉพาะเมื่อมีชนิดสินทรัพย์ที่เหมือนกันอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a23c1-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="a23c1-112">สินทรัพย์ที่คุณกู้ยืมต้องมีสถานะของวงจรการใช้ของสินทรัพย์ที่อนุญาตให้ใช้เป็นสินทรัพย์ที่ให้ยืม เช่น **InStorage**</span><span class="sxs-lookup"><span data-stu-id="a23c1-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="a23c1-113">เมื่อมีการลงทะเบียนสินทรัพย์ที่ยืม สถานะของวงจรการใช้ของสินทรัพย์จะถูกปรับปรุงโดยอัตโนมัติเป็น ตัวอย่างเช่น **OnLoan**</span><span class="sxs-lookup"><span data-stu-id="a23c1-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="a23c1-114">หากต้องการดูรายการของสินทรัพย์ทั้งหมดที่คุณให้ยืมแก่สถานที่หรือลูกค้าอื่นๆ ให้เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์ที่ยืม** \> **สินทรัพย์ที่ยืมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a23c1-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="a23c1-115">ถ้ามีการเลือกกล่องกาเครื่องหมาย **สิ้นสุด** สำหรับสินทรัพย์ จะมีการลงทะเบียนสินทรัพย์เป็นส่งคืนให้กับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="a23c1-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![จัดการคำขอการบำรุงรักษา](media/06-manage-maintenance-requests.png)

<span data-ttu-id="a23c1-117">ในหน้า **สินทรัพย์ที่ยืมที่ใช้งานอยู่** คุณสามารถดูรายการของสินทรัพย์ที่ให้ยืมทั้งหมดที่ยังไม่ได้ส่งคืนให้กับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="a23c1-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="a23c1-118">ลงทะเบียนสินทรัพย์ที่ให้ยืมเป็นส่งคืน</span><span class="sxs-lookup"><span data-stu-id="a23c1-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="a23c1-119">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์ที่ยืม** \> **สินทรัพย์ที่ยืมที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="a23c1-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="a23c1-120">เลือกสินทรัพย์ที่ยืมที่จะลงทะเบียนเป็นส่งคืน และจากนั้น เลือก **ส่งคืนสินทรัพย์ที่ยืม**</span><span class="sxs-lookup"><span data-stu-id="a23c1-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="a23c1-121">ในฟิลด์ **ส่งคืน** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a23c1-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="a23c1-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a23c1-122">Select **OK**.</span></span>
5. <span data-ttu-id="a23c1-123">รีเฟรชหน้ารายการ **สินทรัพย์ที่ยืมที่ใช้งานอยู่** และสังเกตว่าสินทรัพย์ที่ยืมไม่ปรากฏในรายการอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="a23c1-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
