---
title: เพิ่มฟิลด์ข้อมูลในการรวมภาษีโดยใช้ส่วนขยาย
description: บทความนี้อธิบายวิธีการใช้ส่วนขยาย X++ เพื่อเพิ่มฟิลด์ข้อมูลในการรวมภาษี
author: qire
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 184012dcc0b68e017bb28d8d73caa9e8415bdbfa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871062"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>เพิ่มฟิลด์ข้อมูลในการรวมภาษีโดยใช้ส่วนขยาย

[!include [banner](../includes/banner.md)]


บทความนี้อธิบายวิธีการใช้ส่วนขยาย X++ เพื่อเพิ่มฟิลด์ข้อมูลในการรวมภาษี ฟิลด์เหล่านี้สามารถขยายไปยังรูปแบบข้อมูลภาษีของบริการภาษี และใช้เพื่อระบุรหัสภาษี สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ฟิลด์เพิ่มข้อมูลในการตั้งค่าคอนฟิกภาษี](tax-service-add-data-fields-tax-configurations.md)

## <a name="data-model"></a>แบบจำลองข้อมูล

ข้อมูลในรูปแบบข้อมูลจะมีการดําเนินการโดยออบเจ็กต์และใช้งานโดยคลาส

ต่อไปนี้เป็นรายการของออบเจ็กต์หลัก:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

รูปภาพประกอบต่อไปนี้แสดงวิธีที่ออบเจ็กต์เหล่านี้เกี่ยวข้อง

[![ความสัมพันธ์ของออบเจ็กต์รูปแบบข้อมูล](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

ออบเจ็กต์ **เอกสาร** อาจประกอบด้วยออบเจ็กต์ **รายการ** หลายรายการ แต่ละออบเจ็กต์จะประกอบด้วยข้อมูลเมตาสำหรับบริการภาษี

- `TaxIntegrationDocumentObject` มีข้อมูลเมตา `originAddress` ซึ่งมีข้อมูลเกี่ยวกับที่อยู่ต้นทาง และข้อมูลเมตา `includingTax` ซึ่งบ่งชี้ว่ายอดเงินในรายการรวมภาษีขายหรือไม่
- `TaxIntegrationLineObject` มีข้อมูลเมตา `itemId`, `quantity` และ `categoryId`

> [!NOTE]
> `TaxIntegrationLineObject` ยังใช้ออบเจ็กต์ **ค่าธรรมเนียม** ด้วย

## <a name="integration-flow"></a>โฟลว์การรวม

ข้อมูลในโฟลว์จะถูกจัดการโดยกิจกรรม

### <a name="key-activities"></a>กิจกรรมหลัก

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

กิจกรรมจะรันตามลำดับต่อไปนี้:

1. การดึงข้อมูลการตั้งค่า
2. การดึงข้อมูล
3. บริการคำนวณ
4. การแลกเปลี่ยนสกุลเงิน
5. การยังคงอยู่ของข้อมูล

ตัวอย่างเช่น ขยาย **การดึงข้อมูล** ก่อน **บริการคํานวณ**

#### <a name="data-retrieval-activities"></a>กิจกรรมการดึงข้อมูล

กิจกรรม **การดึงข้อมูล** จะดึงข้อมูลจากฐานข้อมูล ตัวปรับต่อสำหรับธุรกรรมต่างๆ จะพร้อมใช้งานเพื่อดึงข้อมูลจากตารางธุรกรรมต่างๆ:

- AxClass/TaxIntegration **PurchTable** DataRetarival
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

ในกิจกรรม **การดึงข้อมูล** เหล่านี้ ข้อมูลจะถูกคัดลอกจากฐานข้อมูลไปยัง `TaxIntegrationDocumentObject` และ `TaxIntegrationLineObject` เนื่องจากกิจกรรมเหล่านี้ทั้งหมดขยายคลาสเทมเพลตนามธรรมเดียวกัน จึงมีวิธีการที่เหมือนกัน

#### <a name="calculation-service-activities"></a>กิจกรรมการบริการคำนวณ

กิจกรรม **บริการคํานวณ** คือลิงค์ระหว่างบริการภาษีและการรวมภาษี กิจกรรมนี้จะรับผิดชอบฟังก์ชันต่อไปนี้:

1. สร้างคำขอ
2. ลงรายการบัญชีการร้องขอไปยังบริการภาษี
3. รับการตอบสนองจากบริการภาษี
4. แยกวิเคราะห์การตอบสนอง

ฟิลด์ข้อมูลที่คุณเพิ่มลงในการร้องขอ จะมีการลงรายการบัญชีพร้อมกับข้อมูลเมตาอื่นๆ 

## <a name="extension-implementation"></a>การใช้งานส่วนขยาย

ส่วนนี้แสดงขั้นตอนโดยละเอียดที่อธิบายวิธีการใช้ส่วนขยาย ซึ่งจะใช้มิติทางการเงิน **ศูนย์ต้นทุน** และ **โครงการ** เป็นตัวอย่าง

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>ขั้นตอนที่ 1 เพิ่มตัวแปรข้อมูลในคลาสออบเจ็กต์

คลาสออบเจ็กต์ประกอบด้วยตัวแปรข้อมูลและวิธีการของตัวรับ/ตัวเซ็ตสำหรับข้อมูล เพิ่มฟิลด์ข้อมูลไปยัง `TaxIntegrationDocumentObject` หรือ `TaxIntegrationLineObject` อย่างใดอย่างหนึ่ง โดยขึ้นอยู่กับระดับของฟิลด์ ตัวอย่างต่อไปนี้ใช้ระดับรายการ และชื่อไฟล์คือ `TaxIntegrationLineObject_Extension.xpp`

> [!NOTE]
> ถ้าฟิลด์ข้อมูลที่คุณกำลังเพิ่มอยู่ในระดับเอกสาร ให้เปลี่ยนชื่อไฟล์เป็น `TaxIntegrationDocumentObject_Extension.xpp`

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**ศูนย์ต้นทุน** และ **โครงการ** มีการเพิ่มเป็นตัวแปรส่วนตัว สร้างวิธีการของตัวรับ/ตัวเซ็ตสำหรับฟิลด์ข้อมูลเหล่านี้เพื่อจัดการข้อมูล

### <a name="step-2-retrieve-data-from-the-database"></a>ขั้นตอนที่ 2 ดึงข้อมูลจากฐานข้อมูล

ระบุธุรกรรม และขยายคลาสตัวปรับต่อร์ที่เหมาะสมเพื่อดึงข้อมูล ตัวอย่างเช่น ถ้าคุณใช้ธุรกรรม **ใบสั่งซื้อ** คุณต้องขยาย `TaxIntegrationPurchTableDataRetrieval` และ `TaxIntegrationVendInvoiceInfoTableDataRetrieval` 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` สืบทอดมาจาก `TaxIntegrationPurchTableDataRetrieval` ซึ่งไม่ควรเปลี่ยนแปลง นอกจากตรรกะของตาราง `purchTable` และ `purchParmTable` จะแตกต่างกัน

ถ้าควรเพิ่มฟิลด์ข้อมูลสำหรับธุรกรรมทั้งหมด ให้ขยายคลาส `DataRetrieval` ทั้งหมด

เนื่องจากกิจกรรม **การดึงข้อมูล** ทั้งหมดขยายคลาสเทมเพลตเดียวกัน โครงสร้างคลาส ตัวแปร และวิธีการจะคล้ายกัน

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

ตัวอย่างต่อไปนี้จะแสดงโครงสร้างพื้นฐาน เมื่อมีการใช้ตาราง `PurchTable`

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

เมื่อมีการเรียกวิธีการ `CopyToDocument` บัฟเฟอร์ `this.purchTable` จะมีอยู่แล้ว วัตถุประสงค์ของวิธีการนี้คือการคัดลอกข้อมูลที่ต้องใช้ทั้งหมดจาก `this.purchTable` ไปยังออบเจ็กต์ `document` โดยใช้วิธีการของตัวเซ็ตที่สร้างขึ้นในคลาส `DocumentObject`

เช่นเดียวกับที่มีบัฟเฟอร์ `this.purchLine` อยู่แล้วในวิธีการ `CopyToLine` วัตถุประสงค์ของวิธีการนี้คือการคัดลอกข้อมูลที่ต้องใช้ทั้งหมดจาก `this.purchLine` ไปยังออบเจ็กต์ `_line` โดยใช้วิธีการของตัวเซ็ตที่สร้างขึ้นในคลาส `LineObject`

วิธีที่ตรงไปตรงมาที่สุดคือการขยายวิธีการ `CopyToDocument` และ `CopyToLine` อย่างไรก็ตาม เราขอแนะนำว่าคุณควรลองใช้วิธีการ `copyToDocumentFromHeaderTable` และ `copyToLineFromLineTable` ก่อน หากไม่ทำงานตามที่คุณต้องการ ให้ใช้วิธีการของคุณเอง และเรียกใน `CopyToDocument` และ `CopyToLine` มีสถานการณ์ทั่วไปสามสถานการณ์ที่คุณอาจใช้วิธีการนี้:

- ฟิลด์ที่ต้องใช้อยู่ใน `PurchTable` หรือ `PurchLine` ในสถานการณ์นี้ คุณสามารถขยาย `copyToDocumentFromHeaderTable` และ `copyToLineFromLineTable` ต่อไปนี้เป็นรหัสตัวอย่าง

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- ข้อมูลที่ต้องใช้ไม่อยู่ในตารางเริ่มต้นของธุรกรรม อย่างไรก็ตาม มีความสัมพันธ์ตัวเชื่อมบางความสัมพันธ์กับตารางเริ่มต้น และต้องใช้ฟิลด์ในรายการส่วนใหญ่ ในสถานการณ์นี้ ให้แทนที่ `getDocumentQueryObject` หรือ `getLineObject` เพื่อสอบถามตารางด้วยความสัมพันธ์ตัวเชื่อม ในตัวอย่างต่อไปนี้ ฟิลด์ **จัดส่งทันที** จะถูกรวมเข้ากับใบสั่งขายที่ระดับรายการ

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    ในตัวอย่างนี้ มีการประกาศบัฟเฟอร์ `mcrSalesLineDropShipment` และมีการกําหนดการสอบถามใน `getLineQueryObject` การสอบถามใช้ความสัมพันธ์ `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId` ขณะที่คุณกำลังขยายในสถานการณ์นี้ คุณสามารถแทนที่ `getLineQueryObject` ด้วยออบเจ็กต์การสอบถามที่สร้างขึ้นของคุณเองได้ อย่างไรก็ตาม บันทึกจุดต่อไปนี้:

    * เนื่องจากค่าที่ส่งคืนของวิธีการ `getLineQueryObject` คือ `SysDaQueryObject` คุณต้องสร้างออบเจ็กต์นี้โดยใช้วิธีการ SysDa
    * ไม่สามารถลบตารางที่มีอยู่ได้

- ข้อมูลที่ต้องใช้เกี่ยวข้องกับตารางธุรกรรมโดยความสัมพันธ์ตัวเชื่อมที่ซับซ้อน หรือความสัมพันธ์ไม่ใช่ความสัมพันธ์แบบหนึ่งต่อหนึ่ง (1:1) แต่เป็นความสัมพันธ์แบบหนึ่งต่อกลุ่ม (1:N) ในสถานการณ์นี้ สิ่งต่างๆ จะซับซ้อนเล็กน้อย สถานการณ์นี้จะใช้กับตัวอย่างของมิติทางการเงิน 

    ในสถานการณ์นี้ คุณสามารถใช้วิธีการของคุณเองเพื่อดึงข้อมูล ต่อไปนี้เป็นรหัสตัวอย่างในไฟล์ `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>ขั้นตอนที่ 3 เพิ่มข้อมูลในการร้องขอ

ขยายวิธีการ `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` หรือ `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` เพื่อเพิ่มข้อมูลในการร้องขอ ต่อไปนี้เป็นรหัสตัวอย่างในไฟล์ `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';
    // private const str IOEnumExample = 'Enum Example';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());

        // If the field to be extended is an enum type, use enum2Symbol to convert an enum variable exampleEnum of ExampleEnumType to a string
        // _destination.SetField(IOEnumExample, enum2Symbol(enumNum(ExampleEnumType), _source.getExampleEnum()));
    }
}
```

ในโค้ดนี้ `_destination` เป็นออบเจ็กต์ตัวตัดคำที่ใช้ในการสร้างการร้องขอ และ `_source` เป็นออบเจ็กต์ `TaxIntegrationLineObject`

> [!NOTE]
> กําหนดชื่อฟิลด์ที่จะใช้ในการร้องขอเป็น **private const str** สตริงควรจะเหมือนกับชื่อโหนด (ไม่ใช่ป้ายชื่อ) ที่เพิ่มในบทความ [เพิ่มฟิลด์ข้อมูลในการตั้งค่าคอนฟิกภาษี](tax-service-add-data-fields-tax-configurations.md)
> 
> ตั้งค่าฟิลด์ในวิธีการ **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** โดยใช้วิธีการ **SetField** ชนิดข้อมูลของพารามิเตอร์ที่สองควรเป็น **string** ถ้าชนิดข้อมูลไม่ใช่ **string** ให้แปลงเป็นสตริง
> ถ้าชนิดข้อมูลเป็น X++ **enum type** เราขอแนะนำให้ใช้วิธีการ **enum2Symbol** เพื่อแปลงค่า enum เป็นสตริง ค่า enum ที่เพิ่มในการตั้งค่าคอนฟิกภาษีควรเหมือนกับชื่อ enum เท่านั้น ต่อไปนี้เป็นรายการความแตกต่างระหว่างค่า enum, ป้ายชื่อ และชื่อ
> 
>   - ชื่อของ enum เป็นชื่อสัญลักษณ์ในโค้ด **enum2Symbol()** สามารถแปลงค่า enum เป็นชื่อได้
>   - ค่า enum เป็นจำนวนเต็ม
>   - ป้ายชื่อของ enum สามารถแตกต่างกันในภาษาที่ต้องการ **enum2Str()** สามารถแปลงค่า enum เป็นป้ายชื่อได้

## <a name="model-dependency"></a>การขึ้นต่อกันของแบบโมเดล

เมื่อสร้างโครงการเสร็จเรียบร้อยแล้ว ให้เพิ่มแบบจำลองการอ้างอิงต่อไปนี้ลงในการขึ้นต่อกันของแบบจำลอง

- ApplicationPlatform
- ApplicationSuite
- กลไกจัดการภาษี
- มิติ หากใช้มิติทางการเงิน
- แบบจำลองที่จําเป็นอื่นๆ ที่อ้างอิงในโค้ด

## <a name="validation"></a>การตรวจสอบความถูกต้อง

เมื่อเสร็จสิ้นขั้นตอนก่อนหน้านี้ว คุณสามารถตรวจสอบความถูกต้องของการเปลี่ยนแปลงได้

1. ใน Finance ไปที่ **บัญชีเจ้าหนี้** และเพิ่ม **&debug=vs%2CconfirmExit&** ลงใน URL ตัวอย่างเช่น `https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&` **&** ขั้นสุดท้ายเป็นสิ่งจำเป็น
2. เปิดหน้า **ใบสั่งซื้อ** และเลือก **ใหม่** เพื่อสร้างใบสั่งซื้อ
3. ตั้งค่าฟิลด์ที่ปรับแต่ง แล้วเลือก **ภาษีขาย** จะมีการดาวน์โหลดไฟล์การแก้ไขปัญหาที่มีคำนำหน้า **TaxServiceTroubleshootingLog** โดยอัตโนมัติ ไฟล์นี้ประกอบด้วยข้อมูลธุรกรรมที่ลงรายการบัญชีไปยังบริการคํานวณภาษี 
4. ตรวจสอบว่าฟิลด์ที่ปรับแต่งที่เพิ่มมีอยู่ในส่วน **JSON อินพุตการคำนวณของบริการภาษี** และค่าถูกต้องหรือไม่ ถ้าค่าไม่ถูกต้อง ให้ตรวจสอบขั้นตอนในเอกสารนี้อีกครั้ง

ตัวอย่าง:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>ภาคผนวก

ภาคผนวกนี้แสดงรหัสตัวอย่างที่สมบูรณ์ของการรวมของมิติทางการเงิน **ศูนย์ต้นทุน** และ **โครงการ** ที่ระดับรายการ

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
