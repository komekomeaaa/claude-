---
name: testing
description: テストコードの生成と改善を行う。単体テスト、統合テスト、E2Eテストの作成。テストカバレッジの向上、テスト戦略の立案を支援する。
---

# テストスキル

## 概要

既存コードに対するテストコードの生成、テスト戦略の立案を行うスキルです。

## テストの種類

### 1. 単体テスト (Unit Test)
- 関数・メソッド単位のテスト
- モック/スタブを使用した依存関係の分離
- エッジケースのカバー

### 2. 統合テスト (Integration Test)
- 複数コンポーネントの連携テスト
- API エンドポイントのテスト
- データベース操作のテスト

### 3. E2E テスト (End-to-End Test)
- ユーザーシナリオベースのテスト
- ブラウザ操作のテスト

## テスト生成ルール

1. **AAA パターン**: Arrange → Act → Assert
2. **テスト名**: 「〇〇の場合、△△であること」の形式
3. **1テスト1アサーション**: 原則として1テストケースに1つの検証
4. **エッジケース**: 境界値、null、空配列、異常系を必ず含める

## テンプレート

```typescript
describe('対象のクラス/関数名', () => {
  describe('メソッド名', () => {
    it('正常系: 期待する動作の説明', () => {
      // Arrange
      const input = ...;

      // Act
      const result = targetFunction(input);

      // Assert
      expect(result).toBe(expected);
    });

    it('異常系: エラーケースの説明', () => {
      // Arrange & Act & Assert
      expect(() => targetFunction(invalidInput)).toThrow(ExpectedError);
    });
  });
});
```

## 使用例

```
/testing src/utils/calculator.ts
```
