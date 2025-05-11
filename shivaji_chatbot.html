import React, { useState, useEffect, useRef } from 'react';
import { Card, CardContent } from '@/components/ui/card';
import { Input } from '@/components/ui/input';
import { Button } from '@/components/ui/button';
import { motion } from 'framer-motion';
import { useSpeechRecognition } from 'react-speech-recognition';

// FAQ Data with 5 FAQs
const faqData = [
  {
    question: { hi: "छत्रपति शिवाजी महाराज कौन थे?", en: "Who was Chhatrapati Shivaji Maharaj?" },
    answer: { hi: "छत्रपति शिवाजी महाराज 17वीं सदी के भारतीय योद्धा राजा और मराठा साम्राज्य के संस्थापक थे।", en: "Chhatrapati Shivaji Maharaj was a 17th-century Indian warrior king and the founder of the Maratha Empire." }
  },
  {
    question: { hi: "शिवाजी महाराज का राज्याभिषेक कब हुआ था?", en: "When was Shivaji Maharaj crowned?" },
    answer: { hi: "शिवाजी महाराज का राज्याभिषेक 6 जून 1674 को रायगढ़ किले में हुआ था।", en: "Shivaji Maharaj was crowned on 6th June 1674 at Raigad Fort." }
  },
  {
    question: { hi: "शिवाजी महाराज की मुख्य रणनीतियाँ क्या थीं?", en: "What were the key strategies of Shivaji Maharaj?" },
    answer: { hi: "शिवाजी महाराज की मुख्य रणनीतियाँ गेरिल्ला युद्ध, नौसेना की सशक्तता, किले का प्रबंधन और तेज़ घुड़सवार सेना थीं।", en: "Shivaji Maharaj’s key strategies were guerrilla warfare, a strong navy, fort management, and swift cavalry." }
  },
  {
    question: { hi: "शिवाजी महाराज का सबसे प्रसिद्ध किला कौन सा है?", en: "Which is the most famous fort of Shivaji Maharaj?" },
    answer: { hi: "शिवाजी महाराज का सबसे प्रसिद्ध किला 'रायगढ़ किला' है, जो उनकी राजधानी था।", en: "The most famous fort of Shivaji Maharaj is 'Raigad Fort', which was his capital." }
  },
  {
    question: { hi: "क्या शिवाजी महाराज ने मुगलों के खिलाफ युद्ध किया?", en: "Did Shivaji Maharaj fight against the Mughals?" },
    answer: { hi: "हाँ, शिवाजी महाराज ने मुगलों के खिलाफ कई युद्ध लड़े, जिनमें सबसे प्रसिद्ध 'सिंहगढ़ किला युद्ध' और 'साम्भाजी किला युद्ध' थे।", en: "Yes, Shivaji Maharaj fought several wars against the Mughals, the most famous being the 'Sinhagad Fort Battle' and 'Sambhaji Fort Battle'." }
  },
];

export default function ShivajiChatbot() {
  const [input, setInput] = useState('');
  const [response, setResponse] = useState('आपका प्रश्न पूछें...');
  const [language, setLanguage] = useState('hi-IN');
  const [isProcessing, setIsProcessing] = useState(false); // Track if processing is happening
  const inputRef = useRef(null);

  const { transcript, resetTranscript, listening, startListening, stopListening } = useSpeechRecognition();

  // Function to find the answer from FAQ data
  const getAnswer = (inputText) => {
    const searchText = inputText.toLowerCase();
    const found = faqData.find(faq => 
      faq.question[language.startsWith('hi') ? 'hi' : 'en'].toLowerCase().includes(searchText)
    );

    if (found) {
      return found.answer[language === 'hi-IN' ? 'hi' : 'en'];
    } else {
      return language === 'hi-IN' 
        ? 'मुझे क्षमा करें, मेरे पास इस प्रश्न का उत्तर नहीं है। कृपया कोई और प्रश्न पूछें।' 
        : 'Sorry, I do not have an answer for that. Please ask another question.';
    }
  };

  // Speech Synthesis
  const speakText = (text, lang) => {
    const utterance = new SpeechSynthesisUtterance(text);
    utterance.lang = lang;
    window.speechSynthesis.speak(utterance);
  };

  // Handle the user's input (text or voice)
  const handleAsk = () => {
    if (isProcessing) return; // Prevent new question if already processing
    setIsProcessing(true); // Set processing flag to true

    const answer = getAnswer(input || transcript);
    setResponse(answer);
    speakText(answer, language);

    setIsProcessing(false); // Reset processing flag after answering
  };

  useEffect(() => {
    if (transcript) {
      handleAsk();
    }
  }, [transcript]);

  return (
    <div className="flex flex-col items-center p-4">
      <motion.img
        src="https://img.freepik.com/premium-psd/smiling-3d-cartoon-man-avatar_975163-755.jpg" // Avatar Image
        alt="Shivaji Maharaj Avatar"
        className="w-56 h-56 rounded-full shadow-lg mb-4"
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 1 }}
      />

      <Card className="w-full max-w-md p-4">
        <CardContent>
          <h1 className="text-xl font-bold mb-2 text-center">
            {language === 'hi-IN' ? 'शिवाजी महाराज से पूछें' : 'Ask Shivaji Maharaj'}
          </h1>

          <Button
            variant="outline"
            className="w-full mb-2"
            onClick={() => setLanguage(prev => (prev === 'hi-IN' ? 'en-IN' : 'hi-IN'))}
          >
            🌐 {language === 'hi-IN' ? 'Switch to English' : 'हिंदी में बदलें'}
          </Button>

          <Input
            ref={inputRef}
            placeholder={language === 'hi-IN' ? 'अपना प्रश्न लिखें...' : 'Type your question...'}
            value={input}
            onChange={(e) => setInput(e.target.value)}
            onKeyDown={(e) => { if (e.key === 'Enter') handleAsk(); }}
            className="mb-2"
            aria-label="प्रश्न इनपुट"
          />

          <Button
            onClick={handleAsk}
            className="w-full mb-2 bg-[#ff6600] hover:bg-[#e65c00]"
          >
            {language === 'hi-IN' ? 'पूछें' : 'Ask'}
          </Button>

          {/* Mic Button */}
          <Button
            onClick={listening ? stopListening : startListening}
            className={`w-full mb-2 ${listening ? 'bg-red-500' : 'bg-green-600'} hover:opacity-90`}
          >
            🎤 {listening ? (language === 'hi-IN' ? 'सुन रहा हूँ...' : 'Listening...') : (language === 'hi-IN' ? 'आवाज़ से पूछें' : 'Speak to Ask')}
          </Button>

          <div className="min-h-20 p-2 border rounded bg-gray-100 text-center text-lg">
            {response}
          </div>
        </CardContent>
      </Card>
    </div>
  );
}
