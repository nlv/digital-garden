---
title: Привет
---

# Это мой цифровой сад

Вот [[test1|первая тестовая страница]]

> [!NOTE] Вторая страница внутри: [[Вторая внутри]]


Код на haskell:

```haskell
-- Пример: быстрая сортировка Хоара (QuickSort) на Haskell (~20 строк)
{-# LANGUAGE ScopedTypeVariables #-}

quickSort :: Ord a => [a] -> [a]
quickSort []     = []
quickSort [x]    = [x]
quickSort (x:xs) = 
  let (smaller, larger) = partition (< x) xs
      equal    = filter (== x) xs
  in  quickSort smaller ++ (x : equal) ++ quickSort larger

-- Пример использования с монадой IO
main :: IO ()
main = do
  putStrLn "Исходный список: [5,2,9,1,5,6]"
  let sorted = quickSort [5,2,9,1,5,6] :: [Int]
  putStrLn $ "Отсортировано: " ++ show sorted
  -- Результат: [1,2,5,5,6,9]

-- Дополнительно: работа с Maybe монадой
safeDiv :: Int -> Int -> Maybe Int
safeDiv _ 0 = Nothing
safeDiv x y = Just (x `div` y)

-- Тестирование
testDiv = do
  print $ safeDiv 10 2  -- Just 5
  print $ safeDiv 10 0  -- Nothing
```
