# -Sentiment-Analysis-for-Financial-News
Perform OCR based web scraping for news headlines using QWEN and developing a RAG architecture with QWQ-Latest for text processing and sentiment analysis to predict stock trends.

Step 1: Automate the login process for IBKR TWS using Python and GUI automation tools like PyAutoGUI and OpenCV. 

Step 2: Capture a screenshot of news headlines from IBKR and then extract text from the image using OCR (Optical Character Recognition) with the QWEN model.

Step 3: Process the screenshots and extract headlines in a structured JSON format."content": [
                        {
                            "type": "text",
                            "text": """Analyze the text in the image and extract the headlines into a JSON array. Each line in the image represents a headline and follows a specific format: Time Source [Symbol]/[Company name] Headline.

                                            If a symbol is present, extract it. If no symbol is present, the value for the 'symbol' field in the JSON should be 'na'.
                                            If a company name is present, extract it. If no company is present, the value for the 'company' field in the JSON should be 'na'.
                                            Source is always present for each line so it should not be  empty.
                                            The JSON array should contain objects with the following keys for each headline:

                                            - 'time': The time mentioned at the beginning of the line.
                                            - 'source': The source of the headline, appearing after the time.
                                            - 'symbol': The stock symbol if present, otherwise 'na'.
                                            - 'company': The name of company, otherwise 'na'.
                                            - 'headline': The full text of the headline.

                                  }
                                          
