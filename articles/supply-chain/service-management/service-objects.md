---
title: ภาพรวมของวัตถุที่ให้บริการ
description: 'ออบเจ็กต์บริการคือสินทรัพย์ของลูกค้าและผลิตภัณฑ์ที่คุณสามารถใช้ดำเนินการให้บริการได้ '
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dae74ebb59d73e1197426757ec9c050b1905852e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211801"
---
# <a name="service-objects-overview"></a><span data-ttu-id="c0b85-103">ภาพรวมของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="c0b85-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0b85-104">ออบเจ็กต์บริการคือสินทรัพย์ของลูกค้าและผลิตภัณฑ์ที่คุณสามารถใช้ดำเนินการให้บริการได้ </span><span class="sxs-lookup"><span data-stu-id="c0b85-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="c0b85-105">วัตถุอาจเป็นสิ่งที่สามารถจับต้องได้หรือไม่ก็ได้ ทั้งนี้ขึ้นอยู่กับชนิดการบริการของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0b85-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="c0b85-106">วัตถุที่สามารถจับต้องได้คือสิ่งที่เป็นรูปธรรม เช่น เครื่องจักรหรืออาคาร ซึ่งคุณสามารถใช้ดำเนินการภารกิจการให้บริการทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="c0b85-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="c0b85-107">ออบเจ็กต์ที่ให้บริการแบบมีตัวตนยังอาจเป็นสินค้าในสินค้าคงคลังที่คุณสร้างไว้ในแบบฟอร์มรายละเอียดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="c0b85-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="c0b85-108">คุณสามารถสร้างวัตถุที่ให้บริการได้จนถึงระดับข้อมูลที่มีหมายเลขลำดับประจำสินค้า ทั้งนี้ขึ้นอยู่กับกลุ่มมิติสินค้าคงคลังที่คุณแนบไว้กับสินค้านั้นๆ </span><span class="sxs-lookup"><span data-stu-id="c0b85-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="c0b85-109">วิธีนี้จะมีประโยชน์เมื่อคุณต้องการติดตามสินค้าที่วัตถุที่ให้บริการแสดงถึง </span><span class="sxs-lookup"><span data-stu-id="c0b85-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="c0b85-110">วัตถุที่ให้บริการที่มีตัวตนยังสามารถเป็นสินค้าที่ไม่เกี่ยวข้องโดยตรงกับการผลิตโดยตรงของบริษัท หรือห่วงโซ่การจัดหาวัสดุ </span><span class="sxs-lookup"><span data-stu-id="c0b85-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="c0b85-111">ตัวอย่างเช่น ชุดเครื่องมือที่ใช้สำหรับการซ่อมแซมใบสั่งบริการสามารถเป็นวัตถุที่ให้บริการที่ไม่ได้รวมอยู่ในสินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="c0b85-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="c0b85-112">ในกรณีนี้คุณไม่ต้องลงทะเบียนไว้เป็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="c0b85-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="c0b85-113">วัตถุที่ไม่สามารถจับต้องได้คือสิ่งที่เป็นนามธรรม เช่น ชุดบัญชีหรือเอกสารทางกฎหมายที่คุณสามารถทำงานบริการที่ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c0b85-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="c0b85-114">ตัวอย่างของวัตถุที่ให้บริการที่ไม่มีตัวตน</span><span class="sxs-lookup"><span data-stu-id="c0b85-114">Example of an intangible service object</span></span>

<span data-ttu-id="c0b85-115">บริษัท A รักษาเรกคอร์ดทางการเงินให้กับบริษัทขนาดเล็กจำนวนหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="c0b85-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="c0b85-116">ลูกค้ารายหนึ่งของบริษัท A เป็นทีมฟุตบอลประจำท้องถิ่น ซึ่งบริษัทรับผิดชอบการทำบัญชีประจำสัปดาห์และตรวจสอบบัญชีประจำปีของสโมสร </span><span class="sxs-lookup"><span data-stu-id="c0b85-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="c0b85-117">บัญชีของสโมสรถูกตั้งค่าไว้ในแบบฟอร์มออบเจ็กต์ที่ให้บริการ และถูกกำหนดเป็นออบเจ็กต์ในข้อตกลงการให้บริการ </span><span class="sxs-lookup"><span data-stu-id="c0b85-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="c0b85-118">โดยมีรายการข้อตกลงการให้บริการสองรายการสำหรับวัตถุ </span><span class="sxs-lookup"><span data-stu-id="c0b85-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="c0b85-119">รายการ 1 เป็นการทำบัญชีประจำสัปดาห์ซึ่งมีระยะเวลาห่างหนึ่งครั้งต่อสัปดาห์ ในขณะที่รายการ 2 เป็นการตรวจสอบบัญชีประจำปีซึ่งมีระยะเวลาห่างหนึ่งครั้งต่อปี</span><span class="sxs-lookup"><span data-stu-id="c0b85-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0b85-120">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c0b85-120">Related topics</span></span>

[<span data-ttu-id="c0b85-121">การสร้างวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="c0b85-121">Create service objects</span></span>](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]