# Ubicación de Datos relevantes en el estándar DIAN-XML 

Estas rutas se encuentran expresadas el lenguaje XPath que es el estándar para indicar las
ubicaciones dentro de un documento XML.

| Dato                           | Ubicación                                            |
| ------------------------------ | ---------------------------------------------------- |
| cufe                           | cbc:UUID                                    |
| numero                         | cbc:ID                                    |
| fecha                          | cbc:IssueDate                                    |
| fecha_vencimiento              | cac:PaymentMeans/cbc:PaymentDueDate                                    |
| moneda                         | cbc:DocumentCurrencyCode                                    |
| notas                          | cbc:Note                                    |
| medio_pago                     | cac:PaymentMeans/cbc:PaymentMeansCode                                    |
| forma_pago                     | cac:PaymentMeans/cbc:ID                                    |
| tipo_documento                 | cbc:InvoiceTypeCode                                    |
| version                        | cbc:ProfileID                                    |
| tipo_documento_facturador      | cac:AccountingSupplierParty/cac:Party/cac:PartyTaxScheme/cbc:CompanyID/@schemeName |
| documento_facturador           | cac:AccountingSupplierParty/cac:Party/cac:PartyTaxScheme/cbc:CompanyID                                    |
| nombre_facturador              | cac:AccountingSupplierParty/cac:Party/cac:PartyTaxScheme/cbc:RegistrationName                                    |
| ciudad_facturador              | cac:AccountingSupplierParty/cac:Party/cac:PhysicalLocation/cac:Address/cbc:ID             |
| depto_facturador               | cac:AccountingSupplierParty/cac:Party/cac:PhysicalLocation/cac:Address/cbc:CountrySubentity |
| direccion_facturador           | cac:AccountingSupplierParty/cac:Party/cac:PhysicalLocation/cac:Address/cac:AddressLine |
| email_facturador               | cac:AccountingSupplierParty/cac:Party/cac:Contact/cbc:ElectronicMail                                    |
| tipo_persona_facturador        | cac:AccountingSupplierParty/cbc:AdditionalAccountID                                |
| tipo_documento_adquiriente     | cac:AccountingCustomerParty/cac:Party/cac:PartyLegalEntity/cbc:CompanyID/@schemeName |
| documento_adquiriente          | cac:AccountingCustomerParty/cac:Party/cac:PartyLegalEntity/cbc:CompanyID                                    |
| nombre_adquiriente             | cac:AccountingCustomerParty/cac:Party/cac:PartyLegalEntity/cbc:RegistrationName                                    |
| ciudad_adquiriente             | cac:AccountingCustomerParty/cac:Party/cac:PhysicalLocation/cac:Address/cbc:ID             |
| depto_adquiriente              | cac:AccountingCustomerParty/cac:Party/cac:PhysicalLocation/cac:Address/cbc:CountrySubentityCode |
| direccion_adquiriente          | cac:AccountingCustomerParty/cac:Party/cac:PhysicalLocation/cac:Address/cac:AddressLine |
| email_adquiriente              | cac:AccountingCustomerParty/cac:Party/cac:Contact/cbc:ElectronicMail                                    |
| tipo_persona_adquiriente       | cac:AccountingCustomerParty/cbc:AdditionalAccountID                                |
| codigo                         | cac:CreditNote/cac:Delivery/cac:DeliveryAddress/cbc:ID                                    |
| nombre                         | cac:CreditNote/cac:Delivery/cac:DeliveryAddress/cbc:CityName                                    |
| orden_compra                   | cac:OrderReference/cbc:ID                                    |
| numero_factura                 | cbc:BillingReference/cbc:InvoiceDocumentReference/cbc:ID                                    |
| fecha_factura                  | cbc:BillingReference/cbc:InvoiceDocumentReference/cbc:IssueDate                                    |
| cufe_factura                   | cbc:BillingReference/cbc:InvoiceDocumentReference/cbc:UUID                                    |
| total_impuestos                | sum(cac:TaxTotal/cbc:TaxAmount)                                    |
| total_iva                      | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01']/cbc:TaxAmount)                                  |
| base_iva                       | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01']/cbc:TaxableAmount),'#.#####')     |
| base_iva_19                    | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01'  and *:TaxCategory/*:Percent = 19  |
| total_iva_19                   | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01' and *:TaxCategory/*:Percent = 19]/cbc:TaxAmount) |
| base_iva_5                     | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01'  and *:TaxCategory/*:Percent = 5 ] |
| total_iva_5                    | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01' and *:TaxCategory/*:Percent = 5]/cbc:TaxAmount)  |
| base_iva_0                     | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01'  and *:TaxCategory/*:Percent = 0 ] |
| total_iva_0                    | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='01' and *:TaxCategory/*:Percent = 0]/cbc:TaxAmount)  |
| base_ic                        | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='02']/cbc:TaxableAmount)                              |
| total_ic                       | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='02']/cbc:TaxAmount)                                  |
| base_ica                       | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='03']/cbc:TaxableAmount)                              |
| total_ica                      | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='03']/cbc:TaxAmount)                                  |
| base_inc                       | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='04']/cbc:TaxableAmount)                              |
| total_inc                      | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID='04']/cbc:TaxAmount)                                  |
| total_excluido                 | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID=('ZZ','ZY')]/cbc:TaxAmount)                           |
| base_excluido                  | sum(cac:TaxTotal/cac:TaxSubtotal[*:TaxCategory/*:TaxScheme/*:ID=('ZZ','ZY')]/cbc:TaxableAmount),'#.#### |
| base_descuento                 | sum(cac:AllowanceCharge[ cbc:ChargeIndicator = false() ]/cbc:BaseAmount)                                    |
| razon_descuento                | cac:AllowanceCharge[ cbc:ChargeIndicator = false() ]/cbc:AllowanceChargeReason                                 |
| porcentaje_descuento           | cac:AllowanceCharge[ cbc:ChargeIndicator = false() ]/cbc:MultiplierFactorNumeric                               |
| total_descuento                | sum(cac:AllowanceCharge[ cbc:ChargeIndicator = false() ]/cbc:Amount)                                    |
| base_cargo                     | sum( cac:AllowanceCharge[ cbc:ChargeIndicator = true() ]/cbc:BaseAmount )                                    |
| razon_cargo                    | cac:AllowanceCharge[ cbc:ChargeIndicator = true() ]/cbc:AllowanceChargeReason                                  |
| porcentaje_cargo               | cac:AllowanceCharge[ cbc:ChargeIndicator = true() ]/cbc:MultiplierFactorNumeric                                |
| total_cargo                    | sum( cac:AllowanceCharge[ cbc:ChargeIndicator = true() ]/cbc:Amount )                                    |
| subtotal                       | cac:LegalMonetaryTotal/cbc:LineExtensionAmount                                    |
| total_sin_impuestos            | cac:LegalMonetaryTotal/cbc:TaxExclusiveAmount                                    |
| impuestos                      | sum(cac:TaxTotal/cbc:TaxAmount)                                    |
| cargos_y_descuentos            | cac:LegalMonetaryTotal/cbc:AllowanceTotalAmount                                    |
| gran_total                     | cac:LegalMonetaryTotal/cbc:PayableAmount                                    |
| codigo                         | cac:InvoiceLine/cac:Item/cac:StandardItemIdentification/cbc:ID                                    |
| descripcion                    | cac:InvoiceLine/cac:Item/cbc:Description                                    |
| cantidad                       | cac:InvoiceLine/cbc:InvoicedQuantity                                    |
| precio_unitario                | cac:InvoiceLine/cac:Price/cbc:PriceAmount                                    |
| base_descuento                 | sum(cac:InvoiceLine/cac:AllowanceCharge[ cbc:ChargeIndicator = false() ]/cbc:BaseAmount)                                    |
| porcentaje_descuento           | cac:InvoiceLine/cac:AllowanceCharge[ cbc:ChargeIndicator = false() ]/cbc:MultiplierFactorNumeric                               |
| total_descuento                | sum(cac:InvoiceLine/cac:AllowanceCharge[ cbc:ChargeIndicator = false() ]/cbc:Amount)                                    |
| porcentaje_impuesto            | cac:InvoiceLine/cac:TaxTotal/cac:TaxSubtotal/cac:TaxCategory/cbc:Percent                                    |
| tipo_impuesto                  | cac:InvoiceLine/cac:TaxTotal/cac:TaxSubtotal/cac:TaxCategory/cac:TaxScheme/cbc:Name                                    |
| base_impuesto                  | cac:InvoiceLine/cac:TaxTotal/cac:TaxSubtotal/cbc:TaxableAmount                                    |
| valor_impuesto                 | cac:InvoiceLine/cac:TaxTotal/cac:TaxSubtotal/cbc:TaxAmount                                    |
| valor                          | cac:InvoiceLine/cbc:LineExtensionAmount                                    |
| valor_con_impuestos            | cac:InvoiceLine/cbc:LineExtensionAmount + sum(cac:InvoiceLine/cac:TaxTotal/cac:TaxSubtotal/cbc:TaxAmount)                                    |
