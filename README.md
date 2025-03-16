# Angular Voice Command Plugin

An Angular service that enables voice-based interactions using the Web Speech API. Define voice commands and trigger specific actions in your application.

## Features
- 🎙️ Supports custom voice commands
- 🔄 Continuous speech recognition
- 🌍 Multi-language support (default: `en-US`)
- 🛠️ Simple API for integration

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/angular-voice-command.git
   cd angular-voice-command
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Run the Angular application:
   ```sh
   ng serve
   ```

## Usage
### 1. Import and Inject the Service
```typescript
import { Component } from '@angular/core';
import { VoiceCommandService } from './services/voice-command.service';

@Component({
  selector: 'app-root',
  template: `<button (click)="startVoiceCommands()">Start Voice Commands</button>`,
})
export class AppComponent {
  constructor(private voiceService: VoiceCommandService) {}

  startVoiceCommands() {
    this.voiceService.startListening({
      'hello': () => alert('Hello detected!'),
      'open settings': () => console.log('Opening settings...'),
    });
  }
}
```

### 2. Stopping Voice Recognition
```typescript
this.voiceService.stopListening();
```

## Contributing
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-branch`
3. Commit your changes: `git commit -m "Added new feature"`
4. Push to the branch: `git push origin feature-branch`
5. Open a Pull Request.

## License
MIT License

