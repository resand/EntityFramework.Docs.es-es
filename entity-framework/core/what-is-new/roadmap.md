---
title: Mapa de ruta de Entity Framework Core
author: divega
ms.date: 02/20/2018
ms.assetid: 834C9729-7F6E-4355-917D-DE3EE9FE149E
uid: core/what-is-new/roadmap
ms.openlocfilehash: 937bfff4cbc3ec0b2235a78cb2f1f246697128d5
ms.sourcegitcommit: 87fcaba46535aa351db4bdb1231bd14b40e459b9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2019
ms.locfileid: "59929789"
---
# <a name="entity-framework-core-roadmap"></a>Mapa de ruta de Entity Framework Core

> [!IMPORTANT]
> Tenga en cuenta que los conjuntos de características y las programaciones de las versiones futuras siempre están sujetos a cambios y, aunque intentamos mantener esta página actualizada, es posible que no refleje nuestros planes más recientes en todo momento.

## <a name="ef-core-30"></a>EF Core 3.0

Con EF Core 2.2 ya en el mercado, nuestro objetivo principal es ahora EF Core 3.0.
Vea [Novedades de EF Core 3.0](xref:core/what-is-new/ef-core-3.0/index) para obtener información sobre las [nuevas características](xref:core/what-is-new/ef-core-3.0/features) planeadas y los [cambios importantes](xref:core/what-is-new/ef-core-3.0/breaking-changes) previstos que se incluyen en esta versión.

## <a name="schedule"></a>Programación

La programación de versiones de EF Core está sincronizada con la [programación de versiones de .NET Core](https://github.com/dotnet/core/blob/master/roadmap.md).

## <a name="backlog"></a>Trabajo pendiente

El [hito de trabajo pendiente](https://github.com/aspnet/EntityFrameworkCore/issues?q=is%3Aopen+is%3Aissue+milestone%3ABacklog+sort%3Areactions-%2B1-desc) de nuestro rastreador de problemas contiene dificultades en las que esperamos trabajar algún día o que consideramos que alguien de la comunidad podría abordar.
Los clientes pueden enviar comentarios y votar en relación con estos problemas.
Se alienta a los colaboradores que busquen trabajar en cualquiera de estos temas a que comiencen primero una discusión sobre cómo abordarlos.

Nunca hay una garantía de que trabajaremos en una característica determinada en una versión específica de EF Core.
Al igual que en todos los proyectos de software, pueden cambiar las prioridades, las programaciones de lanzamiento y los recursos disponibles en cualquier momento.
Pero si pretendemos resolver un problema en un período de tiempo específico, lo asignaremos a un hito de lanzamiento en lugar de al hito de trabajo pendiente.
Como parte de nuestro [proceso de planeamiento de versiones](#release-planning-process), movemos periódicamente los problemas entre los hitos de lanzamiento y de trabajo pendiente.

Probablemente cerraremos un problema si no tenemos previsto solucionarlo.
Pero podemos reconsiderar un problema que cerramos previamente si obtenemos nueva información al respecto.

## <a name="release-planning-process"></a>Proceso de planeamiento de versiones

A menudo nos preguntan cómo se eligen características específicas para incluirlas en una versión concreta.
La lista de trabajos pendientes no se corresponde con los planes de versión.
La presencia de una característica en EF6 tampoco implica automáticamente que esta se vaya a implementar en EF Core.

Es difícil detallar todo el proceso que se sigue para planear una versión.
Gran parte consiste en describir las características específicas, las oportunidades y las prioridades, y el propio proceso también evoluciona con cada versión.
Sin embargo, podemos resumir las preguntas comunes que intentamos responder a la hora de decidir en qué elementos trabajaremos a continuación:

1. **¿Cuántos desarrolladores creemos que usarán la característica y en qué medida mejorará las aplicaciones o la experiencia?** Para responder a esta pregunta, recopilamos información de varias fuentes, y los comentarios y los votos son una de ellas.

2. **¿Qué soluciones alternativas pueden adoptar los usuarios si todavía no se ha implementado una característica?** Por ejemplo, hay muchos desarrolladores que pueden asignar una tabla de unión para poder trabajar a pesar de la falta de compatibilidad múltiple de forma nativa. Obviamente, no todos los desarrolladores quieren hacerlo, pero muchos pueden, y eso se considera un factor decisivo.

3. **¿La implementación de esta característica hará evolucionar la arquitectura de EF Core tanto como para poder implementar otras características?** Normalmente tienen preferencia las características que actúan como bloques de creación de otras características. Por ejemplo, las entidades contenedoras de propiedades pueden ayudarnos a avanzar hacia la compatibilidad de varios a varios, y los constructores de entidades han habilitado nuestra compatibilidad de carga diferida.

4. **¿La característica es un punto de extensibilidad?** Los puntos de extensibilidad suelten tener preferencia sobre las características normales porque permiten que los desarrolladores puedan crear sus propios comportamientos y compensar las funcionalidades que faltan.

5. **¿Cuál es la sinergia de la característica cuando se usa en combinación con otros productos?** Tienen preferencia las características que permiten o mejoran significativamente la experiencia de uso de EF Core con otros productos, como .NET Core, la última versión de Visual Studio, Microsoft Azure, etc.

6. **¿Cuáles son las habilidades de las personas disponibles para trabajar en una característica y cómo se aprovechan mejor estos recursos?** Todos los miembros del equipo de EF, e incluso los colaboradores de la comunidad, tienen diferentes niveles de experiencia en varias áreas, y tenemos que elaborar el plan de acuerdo con ello. Incluso aunque quisiéramos tener a todos trabajando en una característica específica, como las traducciones de GroupBy o las relaciones múltiples, no sería práctico.

Como se mencionó antes, el proceso evoluciona con cada versión.
En el futuro, intentaremos agregar más oportunidades para que los miembros de la comunidad proporcionen información sobre nuestros planes de lanzamiento.
Por ejemplo, nos gustaría que fuera más fácil revisar los diseños de borrador de las características y el propio plan de lanzamiento.
