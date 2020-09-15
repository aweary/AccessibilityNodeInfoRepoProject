# AccessibilityNodeInfoRepoProject

This demonstrates the issue described here: https://issuetracker.google.com/u/1/issues/168580256

## Steps to Reproduce

* Run the application on a device with TalkBack (reproduced on a Pixel 3a with Android 10)
* Enable TalkBack
* Focus the TextView in the center of the screen
* Change TalkBack to navigate by word
* Attempt to navigate by word for the TextView

## Expected Results

It should go word-by-word for the text that we set on the `AccessibilityNodeInfo` for the view

## Actual Results

It chops up the words using the spans/word boundaries of the visible text, not the accessible text
