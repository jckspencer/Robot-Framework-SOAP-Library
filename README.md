# Robot-Framework-SOAP-Library
SOAP Library for Robot Framework

## Introduction
The SoapLibrary was created for those who want to use the Robot Framework as if they were using SoapUI, just send the request XML and get the response XML.

## Instalation
TODO `pip install`

## Example

    *** Settings ***
    Library           SoapLibrary
    Library           OperatingSystem

    *** Test Cases ***
    Example
        Create Soap Client    http://ws.correios.com.br/calculador/CalcPrecoPrazo.asmx?wsdl
        ${response}    Call SOAP Method With XML    ${CURDIR}/Request_CalcPrecoPrazo.xml
        ${valor}    Get Data From XML By Tag    ${response}    ValorSemAdicionais
        Log    ${valor}
        should be equal    23,50    ${valor}
        
## Keyword Documentation

TODO      

## Authors
   - **Altran -** [Altran Web Site](https://www.altran.com/us/en/)
   - **Samuel Cabral**
   - **Joao Gomes**
   
## License
This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/Altran-PT-GDC/Robot-Framework-SOAP-Library/blob/master/LICENSE.md) file for details.   