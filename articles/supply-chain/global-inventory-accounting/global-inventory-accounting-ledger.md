---
title: บัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลาง
description: หัวข้อนี้จะอธิบายถึงบัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลาง ซึ่งกําหนดโดยชุดสกุลเงิน ปฏิทิน แบบแผน และการเชื่อมโยงกับนิติบุคคล
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273232"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="4b8b4-103">บัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="4b8b4-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="4b8b4-104">การบัญชีสินค้าคงคลังส่วนกลางมีชุดของบัญชีแยกประเภทของตนเอง</span><span class="sxs-lookup"><span data-stu-id="4b8b4-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="4b8b4-105">ในแต่ละครั้งที่มีการประมวลผลธุรกรรมที่เกี่ยวข้องกับสินค้าคงคลังให้กับนิติบุคคลที่เกี่ยวข้อง ระบบจะลงบัญชีธุรกรรมนั้นในบัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลางตามจํานวนเท่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4b8b4-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="4b8b4-106">บัญชีแยกประเภทมีการประเมินของรายการเดบิตและเครดิต</span><span class="sxs-lookup"><span data-stu-id="4b8b4-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="4b8b4-107">การประเมินเหล่านี้จัดประเภทโดยใช้องค์ประกอบต้นทุนและบัญชีบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="4b8b4-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="4b8b4-108">บัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลางกําหนดโดยชุดสกุลเงิน ปฏิทิน แบบแผน และการเชื่อมโยงกับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="4b8b4-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="4b8b4-109">เมื่อต้องการตั้งค่าบัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลางของคุณ ให้ไปที่ **การบัญชีสินค้าคงคลังส่วนกลาง \> การตั้งค่า \> บัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="4b8b4-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="4b8b4-110">สำหรับแต่ละบัญชีแยกประเภท ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b8b4-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="4b8b4-111">**ชื่อ** – ป้อนชื่อของบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4b8b4-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="4b8b4-112">**คำอธิบาย** – ป้อนคำอธิบายของบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4b8b4-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="4b8b4-113">**ปฏิทินทางการเงิน** – ระบุปฏิทินทางการเงินเกี่ยวกับบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4b8b4-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="4b8b4-114">**ชนิดสกุลเงินและอัตราแลกเปลี่ยน** – ใช้ฟิลด์บนแท็บด่วนนี้เพื่อเลือกสกุลเงินทางบัญชีที่บัญชีแยกประเภทใช้ และชนิดอัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="4b8b4-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="4b8b4-115">สกุลเงินที่คุณเลือกอาจแตกต่างจากสกุลเงินที่นิติบุคคลใช้</span><span class="sxs-lookup"><span data-stu-id="4b8b4-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="4b8b4-116">ในการบัญชีสินค้าคงคลังส่วนกลาง ผู้ใช้สามารถกําหนดบัญชีแยกประเภทการคิดต้นทุนได้มากเท่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4b8b4-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="4b8b4-117">การบัญชีสินค้าคงคลังส่วนกลางสนับสนุนการลงบัญชีสินค้าคงคลังในหลายสกุลเงิน และในการประเมินค่าหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="4b8b4-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="4b8b4-118">ตั้งค่าฟิลด์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="4b8b4-118">Set the following fields:</span></span>

    - <span data-ttu-id="4b8b4-119">**สกุลเงิน** – เลือกสกุลเงินการคิดต้นทุนที่มีการรักษามูลค่าที่เกี่ยวข้องกับสินค้าคงคลังไว้</span><span class="sxs-lookup"><span data-stu-id="4b8b4-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="4b8b4-120">มูลค่าเหล่านี้รวมถึงมูลค่าสินค้าคงคลัง ต้นทุนขาย สินค้าคงคลังในการส่งต่อ และผลต่างทุกชนิด</span><span class="sxs-lookup"><span data-stu-id="4b8b4-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="4b8b4-121">**ชนิดอัตราแลกเปลี่ยน** – เลือกอัตราแลกเปลี่ยนที่ระบบควรใช้เพื่อแปลงยอดเงินธุรกรรมในสกุลเงินของธุรกรรม และต้นทุนมาตรฐานของสินค้าเป็นสกุลเงินการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4b8b4-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="4b8b4-122">**ชื่อแบบแผนการ** – ระบุแบบแผน</span><span class="sxs-lookup"><span data-stu-id="4b8b4-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="4b8b4-123">แบบแผนคือชุดของนโยบายที่กําหนดวิธีการลงบัญชีต้นทุนในบัญชีแยกประเภทนี้</span><span class="sxs-lookup"><span data-stu-id="4b8b4-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="4b8b4-124">**นิติบุคคล** – บัญชีแยกประเภทจะลงบัญชีเอกสารที่จะลงรายการบัญชีไปที่นิติบุคคลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4b8b4-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="4b8b4-125">**เริ่มต้น** – เลือกว่าธุรกรรมสินค้าคงคลังที่สร้างขึ้นก่อนที่บัญชีแยกประเภทจะถูกประมวลผลตามสกุลเงินและแบบแผนการในบัญชีแยกประเภทหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4b8b4-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="4b8b4-126">เลือกค่าใดค่าหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4b8b4-126">Select one of the following values:</span></span>

    - <span data-ttu-id="4b8b4-127">**เรียกใช้แล้ว** – บัญชีแยกประเภทควรประมวลผลธุรกรรมที่สร้างขึ้นก่อนการสร้างบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4b8b4-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="4b8b4-128">**เลิกเรียกใช้แล้ว** – บัญชีแยกประเภทควรประมวลผลธุรกรรมที่สร้างขึ้นหลังการสร้างบัญชีแยกประเภทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4b8b4-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4b8b4-129">คุณจะ **ไม่** สามารถย้อนกลับและตั้งค่าฟิลด์นี้ได้หลังจากที่คุณป้อนเอกสารใหม่</span><span class="sxs-lookup"><span data-stu-id="4b8b4-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="4b8b4-130">**สถานะ** – ระบบจะตั้งค่าสถานะของบัญชีแยกประเภทที่สร้างขึ้นใหม่เป็น *จัดเตรียม* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4b8b4-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
