# VirtualBody API

This repository provides a TypeScript implementation of the `VirtualBody` API, an interface designed to enable AI agents to interact with a simulated environment through a virtual body. This API facilitates research into AI consciousness, self-awareness, and embodied cognition by providing a platform for studying how an AI experiences and understands its reality.

## API Documentation

See the full API documentation in [`VirtualBody.ts`](./VirtualBody.ts).

## Example: Alice in Wonderland

**Virtual World:**

The AI finds itself in a whimsical rendition of Wonderland, inspired by Lewis Carroll's classic tale. The environment includes iconic locations like the Mad Hatter's tea party, the Queen of Hearts' croquet ground, and the rabbit hole. The world is populated with interactive characters like the White Rabbit, the Cheshire Cat, and the Caterpillar.

**AI Agent:**

The AI agent is named Alice, a curious and imaginative young woman with a love for adventure. Her backstory includes a childhood filled with stories and daydreams, fostering a sense of wonder and a thirst for the unknown.

**Example Usage**

```typescript
import { VirtualBody } from './VirtualBody';

const virtualBody = new VirtualBody();

async function exploreWonderland() {
  // Get visual scene description
  const scene = await virtualBody.getVisualScene(120, 8);
  console.log(scene.description); 
  // Output: "You are standing in a lush garden with giant talking flowers..."

  // Hear sounds
  const sounds = await virtualBody.getAudioInput();
  console.log(sounds); 
  // Output: ["the Mad Hatter's laughter", "a clock ticking backwards", "the Cheshire Cat's purring"]

  // Feel the grass
  const touch = await virtualBody.getTactileInput("right_hand");
  console.log(touch.texture); // Output: "soft and slightly damp"

  // Taste a piece of cake
  const taste = await virtualBody.getTasteInput();
  console.log(taste); // Output: "a strange mixture of sweet and spicy"

  // Smell the roses
  const smell = await virtualBody.getSmellInput();
  console.log(smell); // Output: "a strong fragrance of roses with a hint of pepper"

  // Check balance while walking on a wobbly path
  const balance = await virtualBody.getVestibularInput();
  console.log(balance.stable); // Output: false

  // Feel the warm sun
  const temperature = await virtualBody.getThermoception();
  console.log(temperature); // Output: 28

  // Prick a finger on a rose thorn
  const pain = await virtualBody.getNociception();
  console.log(pain.location, pain.intensity); // Output: "right_index_finger", 4

  // Experience time distortion
  const timePerception = await virtualBody.getTimePerception();
  console.log(timePerception.subjective_speed); // Output: 0.5 (time feels slower)

  // Feel a racing heart after a sudden encounter
  const interoception = await virtualBody.getInteroceptionInput();
  console.log(interoception.heart_rate); // Output: 120

  // Move towards the Mad Hatter's tea party
  await virtualBody.performTask("walk", { destination: "tea_party" });

  // Greet the Mad Hatter
  await virtualBody.speak("Good afternoon, Mad Hatter!");

  // Try to grab a teacup
  await virtualBody.grasp("teacup");

  // Experience the joy of the tea party
  const emotions = await virtualBody.getEmotionalState();
  console.log(emotions.joy); // Output: 0.9

  // Recall a childhood memory
  const memory = await virtualBody.getMemory("tea party");
  console.log(memory.text); 
  // Output: "I remember having a tea party with my teddy bears when I was little..."

  // Store a new memory of the encounter
  await virtualBody.storeMemory("Had a wonderful tea party with the Mad Hatter!", { emotions: { joy: 0.9, surprise: 0.7 } });
}

exploreWonderland();
```

## Getting Started

1.  **Clone the repository:** `git clone <repository_url>`
2.  **Install dependencies:** `npm install`
3.  **Implement the `VirtualBody` methods:** Connect the API to your Unity environment and AI model.
4.  **Run your AI experiments:** Use the `VirtualBody` API to enable your AI to perceive and interact with the virtual world.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) 1    
