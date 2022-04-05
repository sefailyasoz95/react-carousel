# Carousel Component for React

Easy to use and TypeScript compatible carousel component.

## Installation

To install the library you can run

```bash
npm install @sefailyasoz/react-carousel # or yarn add @sefailyasoz/react-carousel
```

### Example

You can see the example output from this link: https://ibb.co/4sh1HZH

The Carousel component takes one neseccary prop which is data. This data must be an array of objects and this objects' type is as follows:

> {
> image: string,
> headerText?: string | null,
> subText?: string | null
> }

The props that are shown in this example shown with their default values except leftItem, rightItem and data props.
data prop is mandatory but the others are optional.
leftItem and rightItem props can take any React element as a value. You can use your own custom buttons for the slide navigation
as shown in the example. If you don't give anything, the component will use it is own buttons.

```txt
import { Carousel } from '@sefailyasoz/react-carousel'
import { FaArrowLeft, FaArrowRight } from 'react-icons/fa'
const MyApp = () => {

const CarouselData = [
  {
    headerText: null,
    subText: 'Sub Text One',
    image: 'https://picsum.photos/300/300',
  },
  {
    headerText: 'Header Text Two',
    subText: null,
    image: 'https://picsum.photos/1200/800',
  },
  {
    headerText: null,
    subText: null,
    image: 'https://picsum.photos/720/720',
  },
  {
    headerText: 'Header Text Four',
    subText: 'Sub Text Four',
    image: 'https://picsum.photos/1920/1080',
  },
  {
    headerText: 'Header Text Five',
    subText: 'Sub Text Five',
    image: 'https://picsum.photos/480/360',
  },
]
  return    <Carousel
              data={CarouselData}
              autoPlay={true}
              rightItem={<FaArrowRight />}
              leftItem={<FaArrowLeft />}
              animationDuration={3000}
              headerTextType="black"
              subTextType="white"
              size="normal"
            />
}

export default MyApp
```
