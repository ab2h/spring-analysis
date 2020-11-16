# Spring convert 阅读指南
- 本节主要围绕类型转换接口 `org.springframework.core.convert.converter.Converter` 展开, 
    对接口 `Converter` 做了介绍, 同时也对使用到的其他接口进行了分析, 诸如`ConverterRegistry` 、`ConversionService` 等. 
    
    
    
- 涉及接口类如下
    1. org.springframework.core.convert.converter.ConditionalConverter
    1. org.springframework.core.convert.support.ConfigurableConversionService
    1. org.springframework.core.convert.ConversionService
    1. org.springframework.core.convert.converter.Converter
    1. org.springframework.core.convert.converter.ConverterRegistry
    1. org.springframework.core.convert.support.DefaultConversionService
    1. org.springframework.format.support.DefaultFormattingConversionService
    1. org.springframework.format.FormatterRegistry
    1. org.springframework.format.support.FormattingConversionService
    1. org.springframework.core.convert.support.GenericConversionService
    1. org.springframework.core.convert.converter.GenericConverter
    1. org.springframework.beans.TypeConverter
    1. org.springframework.core.convert.TypeDescriptor
    涉及到的类有些多. 请各位耐心阅读
    
    
- 分析文章: 
    - [Spring-ConditionalConverter](/docs/core/convert/Spring-ConditionalConverter.md)
        - [Spring-AbstractConditionalEnumConverter](/docs/core/convert/ConditionalConverter/Spring-AbstractConditionalEnumConverter.md)
        - [Spring-NumberToNumberConverterFactory](/docs/core/convert/ConditionalConverter/Spring-NumberToNumberConverterFactory.md)
    - [Spring-ConfigurableConversionService](/docs/core/convert/Spring-ConfigurableConversionService.md)
    - [Spring-ConversionService](/docs/core/convert/Spring-ConversionService.md)
    - [Spring-Converter](/docs/core/convert/Spring-Converter.md)
    - [Spring-ConverterRegistry](/docs/core/convert/Spring-ConverterRegistry.md)
    - [Spring-DefaultConversionService](/docs/core/convert/Spring-DefaultConversionService.md)
    - [Spring-DefaultFormattingConversionService](/docs/core/convert/Spring-DefaultFormattingConversionService.md)
    - [Spring-FormatterRegistry](/docs/core/convert/Spring-FormatterRegistry.md)
    - [Spring-FormattingConversionService](/docs/core/convert/Spring-FormattingConversionService.md)
    - [Spring-GenericConversionService](/docs/core/convert/Spring-GenericConversionService.md)
    - [Spring-GenericConverter](/docs/core/convert/Spring-GenericConverter.md)
        - [Spring-NoOpConverter](/docs/core/convert/GenericConverter/Spring-NoOpConverter.md)
        - [Spring-ParserConverter](/docs/core/convert/GenericConverter/Spring-ParserConverter)
        - [Spring-PrinterConverter](/docs/core/convert/GenericConverter/Spring-PrinterConverter)
    - [Spring-TypeConverter](/docs/core/convert/Spring-TypeConverter.md)
        - [Spring-TypeConverterDelegate](/docs/core/convert/TypeConverter/Spring-TypeConverterDelegate.md)
        - [Spring-TypeConverterSupport](/docs/core/convert/TypeConverter/Spring-TypeConverterSupport.md)
    - [Spring-TypeDescriptor](/docs/core/convert/Spring-TypeDescriptor.md)