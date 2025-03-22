import cv2
import numpy as np

cap = cv2.VideoCapture(1)

while True:
    sizeFat = 2
    ret, image = cap.read()
    if not ret:
        break
    allContuors = image
    img1=image
    image = cv2.medianBlur(image, 3)
    cv2.imshow('1', image)
    blackImage = np.zeros((500, 500, 3), dtype=np.uint8)
    # for red image
    lower_red = np.array([20, 0, 110])
    upper_red = np.array([255, 100, 240])
    # image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
    red_mask = cv2.inRange(image, lower_red, upper_red)
    red = cv2.bitwise_and(image, image, mask=red_mask)
    red = cv2.medianBlur(red, 3)
    # cv2.imshow('red', red)
    red = cv2.cvtColor(red, cv2.COLOR_BGR2GRAY)
    contours, _ = cv2.findContours(red, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_NONE)
    print()
    lisd = []
    for contour in contours:
        if 300 < cv2.contourArea(contour) > 50:
            print('lox')
            print(cv2.contourArea(contour)) 
            lisd.append(cv2.contourArea(contour))
            cv2.drawContours(blackImage, [contour], 0, (255, 255, 0), 1)
            blackImage = np.zeros((1000, 1000, 3), dtype=np.uint8)
            epsilon = 0.037 * cv2.arcLength(contour, True)
            approx = cv2.approxPolyDP(contour, epsilon, True)
            if 2500<cv2.contourArea(contour):
                cv2.drawContours(image, [contour], 0, (0, 0, 0), 1)
                cv2.drawContours(allContuors, [contour], 0, (0, 0, 0), 1)
                text = f"ferz white"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(allContuors, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (255, 255, 255), sizeFat)
            elif len(approx) == 5:
                cv2.drawContours(image, [approx], 0, (255, 255, 255), 1)
                cv2.drawContours(allContuors, [approx], 0, (255, 255, 255), 1)
                text = f"peshka white"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(allContuors, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (255, 255, 255), sizeFat)
            elif len(approx) == 4:
                cv2.drawContours(image, [approx], 0, (0, 255, 0), 1)
                cv2.drawContours(allContuors, [approx], 0, (0, 255, 0), 1)
                text = f"korol white"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(allContuors, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (255, 255, 255), sizeFat)
            elif len(approx) == 3:
                cv2.drawContours(image, [approx], 0, (0, 0, 255), 1)
                cv2.drawContours(allContuors, [approx], 0, (0, 0, 255), 1)
                text = f"kon white"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(allContuors, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (255, 255, 255), sizeFat)
            elif len(approx) == 6 or len(approx) == 7:
                
                cv2.drawContours(image, [approx], 0, (255, 125, 125), 1)
                cv2.drawContours(allContuors, [approx], 0, (255, 125, 125), 1)
                text = f"slon white"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(allContuors, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (255, 255, 255), sizeFat)
                # cv2.drawContours(image, [contour], 0, (255, 0, 255), 1)
            elif len(approx) == 8 or len(approx) == 9:
                cv2.drawContours(image, [approx], 0, (0, 255, 255), 1)
                cv2.drawContours(allContuors, [approx], 0, (0, 255, 255), 1)
                text = f"ladya white"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(allContuors, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (255, 255, 255), sizeFat)
            else:
                cv2.drawContours(image, [approx], 0, (255, 0, 0), 1)
                
    # for blue figures
    blackImage = np.zeros((500, 500, 3), dtype=np.uint8)
    lower_blue = np.array([100, 0, 0])
    upper_blue = np.array([170, 160 , 70])
    blue_mask = cv2.inRange(img1, lower_blue, upper_blue)
    blue = cv2.bitwise_and(img1, image, mask=blue_mask)
    blue = cv2.medianBlur(blue,9)
    blue = cv2.cvtColor(blue, cv2.COLOR_BGR2GRAY)
    contours, _ = cv2.findContours(blue, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_NONE)
    for i,contour in enumerate(contours):
        if 300 < cv2.contourArea(contour) > 70:
            
            lisd.append(cv2.contourArea(contour))
            # print()
            cv2.drawContours(blackImage, [contour], 0, (255, 255, 0), 1)
            blackImage = np.zeros((1000, 1000, 3), dtype=np.uint8)
            epsilon = 0.04 * cv2.arcLength(contour, True)
            approx = cv2.approxPolyDP(contour, epsilon, True)
            
            if 2800<cv2.contourArea(contour):
                cv2.drawContours(img1, [contour], 0, (0, 0, 0), 1)
                cv2.drawContours(allContuors, [contour], 0, (0, 0, 0), 1)
                text = f"ferz black"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(img1, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (0, 0, 0), sizeFat)
                print('ferz')
                print(cv2.contourArea(contour)) 
            elif len(approx) == 5:
                cv2.drawContours(img1, [approx], 0, (255, 255, 255), 1)
                cv2.drawContours(allContuors, [approx], 0, (255, 255, 255), 1)
                text = f"peshka black"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(img1, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (0, 0, 0), sizeFat)
                print('peshka')
                print(cv2.contourArea(contour)) 
            elif len(approx) == 4:
                if cv2.contourArea(contour)>1400:
                    cv2.drawContours(img1, [approx], 0, (0, 255, 0), 1)
                    cv2.drawContours(allContuors, [approx], 0, (0, 255, 0), 1)
                    text = f"korol black"
                    x, y, w, h = cv2.boundingRect(contour)
                    center_x = x + w // 2
                    center_y = y + h // 2
                    text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                    text_x = center_x - text_size[0] // 2
                    text_y = center_y + text_size[1] // 2
                    print('korol')
                    print(cv2.contourArea(contour)) 
                    cv2.putText(img1, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (0, 0, 0), sizeFat)
                else:
                    cv2.drawContours(img1, [approx], 0, (0, 0, 255), 1)
                    cv2.drawContours(allContuors, [approx], 0, (0, 0, 255), 1)
                    text = f"kon black"
                    x, y, w, h = cv2.boundingRect(contour)
                    center_x = x + w // 2
                    center_y = y + h // 2
                    text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                    text_x = center_x - text_size[0] // 2
                    text_y = center_y + text_size[1] // 2
                    print('kon sosal')
                    print(cv2.contourArea(contour)) 
                    cv2.putText(img1, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (0, 0, 0), sizeFat)
            elif len(approx) == 3:
                cv2.drawContours(img1, [approx], 0, (0, 0, 255), 1)
                cv2.drawContours(allContuors, [approx], 0, (0, 0, 255), 1)
                text = f"kon black"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(img1, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (0, 0, 0), sizeFat)
                print('kon')
                print(cv2.contourArea(contour)) 
            elif len(approx) == 6 or len(approx) == 7:
                
                cv2.drawContours(img1, [approx], 0, (255, 125, 255), 1)
                cv2.drawContours(allContuors, [approx], 0, (255, 125, 255), 1)
                text = f"slon black"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(img1, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (0, 0, 0), sizeFat)
                print('slon')
                print(cv2.contourArea(contour)) 
                # cv2.drawContours(image, [contour], 0, (255, 0, 255), 1)
            elif len(approx) == 8 or len(approx) == 9:
                cv2.drawContours(img1, [approx], 0, (0, 255, 255), 1)
                cv2.drawContours(allContuors, [approx], 0, (0, 255, 255), 1)
                text = f"ladya black"
                x, y, w, h = cv2.boundingRect(contour)
                center_x = x + w // 2
                center_y = y + h // 2
                text_size = cv2.getTextSize(text, cv2.FONT_HERSHEY_SIMPLEX, 0.1, 2)[0]
                text_x = center_x - text_size[0] // 2
                text_y = center_y + text_size[1] // 2
                cv2.putText(img1, text, (text_x, text_y), cv2.FONT_HERSHEY_SIMPLEX, 0.5, (0, 0, 0), sizeFat)
                print('ladya')
                print(cv2.contourArea(contour)) 
            else:
                cv2.drawContours(img1, [approx], 0, (255, 0, 0), 1)
    cv2.imshow("all contuors", allContuors)
    cv2.waitKey(0)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cv2.destroyAllWindows()
